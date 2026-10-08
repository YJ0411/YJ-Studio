# YJ Studio Website — Bilingual Content Plan

> Website type: React static marketing website hosted on GitHub Pages  
> Languages: English and Chinese  
> Primary goal: Help visitors understand the packages and contact YJ Studio.

## 1. Final website structure

Keep the website small and focused. Use only these pages:

| Page | URL | Purpose |
|---|---|---|
| Home | `/` | About YJ Studio, explain the service, and show all package prices |
| Custom Build | `/custom-build` | Explain custom websites and web applications |
| FAQ | `/faq` | Answer common questions |
| Contact | `/contact` | Receive project enquiries |

There should be no separate Services, Pricing, Process, Portfolio, or About pages for the first version. Their useful content belongs on the Home page.

The Basic Website and Editable Website cards on Home should have **View Demo** buttons. These buttons can link to live demo URLs or temporary placeholders until the demos are ready. The Custom Build card should link to `/custom-build`.

## 2. Language support

### Language switcher

Place a visible language switcher in the header:

- `EN`
- `中文`

Recommended behaviour:

- Default to English.
- Detect Chinese browser language when possible.
- Allow the visitor to change language at any time.
- Save the visitor’s choice in `localStorage`.
- Translate all visible text, navigation labels, buttons, forms, validation messages, page titles, and meta descriptions.
- Do not mix English and Chinese in the same sentence.

Use **Simplified Chinese** (`zh-CN`) for the Chinese version.

### Suggested React content structure

Keep the text in separate language objects instead of hard-coding text inside components:

```js
const content = {
  en: { /* English content */ },
  zh: { /* 中文内容 */ },
};
```

This makes it easier to review translations and add another language later.

## 3. Top navigation bar, shared navigation, and footer

### Top navigation bar layout

The top navigation should appear on every page and remain visually consistent.

#### Desktop layout

Use a single horizontal bar:

```text
[ YJ Studio ]     Home   Packages   FAQ   Contact      EN | 中文   [ Get a Quote ]
```

- Left: YJ Studio logo or wordmark.
- Centre/right: Home, Packages, FAQ, and Contact links.
- Language switcher: `EN | 中文`.
- Right-most primary CTA: **Get a Quote** / **获取报价**.
- Keep the bar compact so it does not take too much vertical space.
- Use a subtle bottom border or shadow rather than a heavy background effect.

#### Mobile layout

Use:

```text
[ YJ Studio ]                         [ ☰ ]
```

When the menu opens, show:

- Home / 首页
- Packages / 配套
- FAQ / 常见问题
- Contact / 联系我们
- EN | 中文
- Get a Quote / 获取报价

The mobile menu should close after a link is selected. The Contact or Get a Quote action should be easy to reach with one tap.

#### Navigation behaviour

- Make the top bar sticky after the visitor scrolls down.
- Add a visible active state for the current page.
- Keep navigation links keyboard accessible.
- Use a clear focus outline for keyboard users.
- Ensure the language switcher is a button or accessible control, not plain text only.
- On the Home page, **Packages** scrolls to the package section. There is no separate Custom Build link in the top navigation; visitors can reach it from the Custom Build card or Home page CTA.
- The logo links back to `/`.

#### Bilingual labels

| English | 中文 | Link |
|---|---|---|
| Home | 首页 | `/` |
| Packages | 配套 | `/#packages` |
| FAQ | 常见问题 | `/faq` |
| Contact | 联系我们 | `/contact` |
| Get a Quote | 获取报价 | `/contact` |

#### Suggested visual styling

- Background: white or a very light neutral colour.
- Text: dark charcoal.
- Accent colour: use the YJ Studio brand colour for the CTA and active link.
- CTA: rounded button with strong contrast.
- Height: approximately 64–76px on desktop and 56–64px on mobile.
- Content width: centred container with a maximum width around 1,200px.

### Header navigation labels

English:

- Home
- Packages
- FAQ
- Contact
- `EN | 中文`
- Button: **Get a Quote**

Chinese:

- 首页
- 配套
- 常见问题
- 联系我们
- `EN | 中文`
- Button: **获取报价**

### Footer

English:

> YJ Studio — Websites and web applications for businesses, professionals, and individuals.

Chinese:

> YJ Studio — 为企业、专业人士和个人打造网站及网页应用。

### Footer contact block

Show a compact contact block in the footer so visitors can reach YJ Studio from any page.

English:

> **Contact us**  
> Email: [YOUR EMAIL ADDRESS]  
> WhatsApp: [YOUR WHATSAPP NUMBER]  
> Based in: [CITY, MALAYSIA]

Chinese:

> **联系我们**  
> 电邮：[YOUR EMAIL ADDRESS]  
> WhatsApp：[YOUR WHATSAPP NUMBER]  
> 所在地：[城市，马来西亚]

Add two small footer buttons:

- **WhatsApp** / **WhatsApp 联系** — opens the WhatsApp link.
- **Email** / **发送电邮** — opens the email client using a `mailto:` link.

Use the same contact details on the Contact page. Replace all placeholders before launch.

Footer links:

- Home / 首页
- Custom Build / 定制开发
- FAQ / 常见问题
- Contact / 联系我们
- Privacy Policy / 隐私政策

Replace these placeholders before launch:

- Email: `[YOUR EMAIL ADDRESS]`
- WhatsApp: `[YOUR WHATSAPP LINK]`
- Social links: `[YOUR SOCIAL LINKS]`

## 4. Home page

### URL

`/`

### SEO metadata

English:

- **Title:** Websites and Web Apps for Malaysian Businesses | YJ Studio
- **Description:** YJ Studio builds professional websites, editable websites, and custom web applications for Malaysian businesses, professionals, and individuals.

Chinese:

- **Title:** 为马来西亚企业打造网站和网页应用 | YJ Studio
- **Description:** YJ Studio 为马来西亚企业、专业人士和个人打造专业网站、可编辑网站及定制网页应用。

### Section 1: Hero

English:

#### Heading

> Build a website that helps your business grow.

#### Supporting text

> YJ Studio helps businesses, professionals, freelancers, and individuals create clear, modern websites and practical web applications.

#### Buttons

- **View Packages** — scroll to the Packages section.
- **Get a Quote** — link to `/contact`.

Chinese:

#### 标题

> 打造帮助业务成长的网站。

#### 说明

> YJ Studio 为企业、专业人士、自由职业者和个人打造清晰、现代的网站及实用的网页应用。

#### 按钮

- **查看配套** — 滚动到配套部分。
- **获取报价** — 前往 `/contact`。

Small trust line:

- English: `React websites • Clear pricing • Hosting setup assistance`
- Chinese: `React 网站 • 价格透明 • 提供主机设置协助`

### Section 2: About YJ Studio

English:

#### Heading

> Technology should make your business simpler.

#### Copy

> YJ Studio is a software development service that helps SMEs, local businesses, professionals, freelancers, and individuals build a professional online presence. We focus on practical solutions, clear project scope, and websites that are easy for clients to understand and use.

> We use React for modern website interfaces and PostgreSQL for projects that need structured business data, such as products, services, users, or admin features.

Chinese:

#### 标题

> 科技应该让您的业务更简单。

#### 内容

> YJ Studio 是一家软件开发服务，为中小企业、本地商家、专业人士、自由职业者和个人打造专业的线上形象。我们专注于实用的解决方案、清晰的项目范围，以及客户容易理解和使用的网站。

> 我们使用 React 打造现代网站界面，并在产品、服务、用户或后台管理等项目中使用 PostgreSQL 管理业务数据。

### Section 3: What we can help with

Use four short cards.

| English | 中文 |
|---|---|
| Business websites | 企业网站 |
| Personal websites and portfolios | 个人网站和作品集 |
| Product or service catalogues | 产品或服务目录 |
| Mobile-friendly web apps | 适合手机使用的网页应用 |
| Custom web applications | 定制网页应用 |

Supporting copy:

- English: `Start with a focused website and expand into a custom system when your business is ready.`
- Chinese: `先从清晰的网站开始，业务发展后再扩展成定制系统。`

### Section 4: Packages and pricing

#### Section heading

- English: **Choose the right starting point**
- Chinese: **选择适合您的起点**

Show all three package cards on the Home page.

#### Card 1: Basic Website

Price:

> From RM2,500

English description:

> A professional website for a business, freelancer, professional, portfolio, or personal brand.

Chinese description:

> 适合企业、自由职业者、专业人士、作品集或个人品牌的专业网站。

Include a short list:

- Up to five core pages / 最多五个主要页面
- Responsive React design / 响应式 React 设计
- Contact or WhatsApp button / 联系表单或 WhatsApp 按钮
- Basic SEO setup / 基础 SEO 设置
- Deployment assistance / 部署协助

Button:

- English: **View Demo**
- Chinese: **查看演示**
- Link: `[BASIC WEBSITE DEMO URL]`

#### Card 2: Editable Website

Price:

> From RM6,500

English description:

> A website with an admin panel so you can update products, services, or content yourself.

Chinese description:

> 配备管理后台，让您可以自行更新产品、服务或网站内容。

Include a short list:

- Admin login / 管理员登录
- Add, edit, publish, and remove content / 添加、编辑、发布和删除内容
- Image upload / 图片上传
- PostgreSQL database / PostgreSQL 数据库
- Admin handover and training / 后台交接和培训

Button:

- English: **View Demo**
- Chinese: **查看演示**
- Link: `[EDITABLE WEBSITE DEMO URL]`

#### Card 3: Custom Build

Price:

> Quote after discovery / 了解需求后报价

English description:

> A custom website, mobile-friendly web app, or full web application for workflows, bookings, dashboards, payments, portals, and integrations.

Chinese description:

> 为工作流程、预约、数据面板、支付、会员门户和系统整合打造定制网站、适合手机使用的网页应用或完整网页应用。

Button:

- English: **Discuss Custom Build**
- Chinese: **咨询定制开发**
- Link: `/custom-build`

### Section 5: Hosting setup assistance

English:

#### Heading

> Need help getting your website online?

#### Copy

> You own the hosting account and pay the hosting provider directly. We can help recommend a provider, set up the account, connect the domain, configure DNS and SSL, and deploy the website for a one-time setup fee.

#### One-time setup guidance

- Provider recommendation and account guidance: **RM150–RM300**.
- Domain, DNS, SSL, and deployment setup: **RM300–RM800**.
- Hosting migration: **from RM500**.

Chinese:

#### 标题

> 需要协助将网站上线吗？

#### 内容

> 主机账户由您拥有，主机费用直接支付给主机服务商。我们可以协助您选择服务商、设置账户、连接域名、配置 DNS 和 SSL，以及部署网站。相关服务收取一次性设置费用。

#### 一次性设置费用参考

- 推荐主机服务商及账户设置指导：**RM150–RM300**。
- 域名、DNS、SSL 和网站部署设置：**RM300–RM800**。
- 主机迁移：**RM500 起**。

Small note:

- English: `Hosting provider fees, domain renewals, and other third-party costs are separate.`
- Chinese: `主机费用、域名续费及其他第三方费用另计。`

### Section 6: Short working approach

Keep this as a small section, not a separate Process page.

| English | 中文 |
|---|---|
| 1. Tell us what you need | 1. 告诉我们您的需求 |
| 2. Confirm the scope and price | 2. 确认范围和价格 |
| 3. Review the website | 3. 查看和反馈网站 |
| 4. Launch with handover | 4. 上线并完成交接 |

### Section 7: Final Home CTA

English:

> Ready to create your website?

> Tell us about your business or idea. We will recommend the most suitable starting point.

Button: **Start Your Enquiry**

Chinese:

> 准备好打造您的网站了吗？

> 告诉我们您的业务或想法，我们会为您推荐合适的起点。

Button: **开始咨询**

## 5. Custom Build page

### URL

`/custom-build`

### SEO metadata

English:

- **Title:** Custom Websites and Web Applications | YJ Studio
- **Description:** YJ Studio builds custom websites, portals, dashboards, booking systems, payment workflows, and web applications.

Chinese:

- **Title:** 定制网站和网页应用 | YJ Studio
- **Description:** YJ Studio 打造定制网站、会员门户、数据面板、预约系统、支付流程及网页应用。

### Hero

- English heading: **Your business is unique. Your software can be too.**
- Chinese heading: **每个业务都不同，您的系统也可以量身定制。**

- English copy: `When a standard package is not enough, we design and build around your workflow, users, and business goals.`
- Chinese copy: `当标准配套无法满足需求时，我们会根据您的工作流程、用户和业务目标进行设计与开发。`

Button:

- English: **Discuss Your Idea**
- Chinese: **讨论您的想法**
- Link: `/contact`

### What we can build

| English | 中文 |
|---|---|
| Booking and appointment systems | 预约和排期系统 |
| Customer or member portals | 客户或会员门户 |
| Admin dashboards and reports | 管理后台和数据报告 |
| Payment and checkout workflows | 支付和结账流程 |
| Internal business tools | 企业内部工具 |
| API and third-party integrations | API 和第三方系统整合 |
| Product and service platforms | 产品和服务平台 |
| Mobile-friendly web apps | 适合手机使用的网页应用 |
| Full web applications | 完整网页应用 |

### Project approach

1. **Discovery / 了解需求** — Understand the business problem and users.
2. **Requirements / 定义需求** — Confirm features, assumptions, and exclusions.
3. **Proposal / 项目方案** — Confirm milestones, timeline, and price.
4. **Build / 开发** — Develop and review the system in stages.
5. **Testing / 测试** — Verify the agreed requirements.
6. **Launch / 上线** — Deploy, train, and hand over the project.

### Free discovery phase

- English: `The initial discovery phase is free. We will discuss your business, understand the problem, identify the likely solution, and recommend the next step before preparing a quotation.`
- Chinese: `初步需求分析免费。我们会了解您的业务和问题，确定可能的解决方案，并在提供报价前建议下一步。`

### Custom Build CTA

- English: `Have an idea but not sure where to start? Send us your requirements and we will help you define the next step.`
- Chinese: `有想法但不知道从哪里开始？把您的需求告诉我们，我们会协助您确定下一步。`

Button: **Contact Us / 联系我们** — `/contact`

## 6. FAQ page

### URL

`/faq`

### SEO metadata

English:

- **Title:** Website Development FAQ | YJ Studio
- **Description:** Answers about YJ Studio packages, pricing, hosting setup, revisions, timelines, and custom development.

Chinese:

- **Title:** 网站开发常见问题 | YJ Studio
- **Description:** 了解 YJ Studio 的网站配套、价格、主机设置、修改次数、项目时间和定制开发服务。

### Questions and answers

#### 1. Do you build personal websites? / 你们制作个人网站吗？

- English: `Yes. The Basic Website package can be used for portfolios, personal brands, professional profiles, resumes, and creator websites.`
- Chinese: `可以。基础网站配套适合作品集、个人品牌、专业介绍、个人简历和创作者网站。`

#### 2. What is the difference between Basic Website and Editable Website? / 基础网站和可编辑网站有什么区别？

- English: `Basic Website is for presenting information. Editable Website includes an admin panel so you can manage products, services, or other content yourself.`
- Chinese: `基础网站主要用于展示信息。可编辑网站包含管理后台，您可以自行管理产品、服务或其他内容。`

#### 3. Do you provide hosting? / 你们提供主机吗？

- English: `We help you choose and set up hosting, but the hosting account belongs to you and you pay the provider directly. Hosting setup is a separate one-time service.`
- Chinese: `我们可以协助您选择和设置主机，但主机账户由您拥有，费用直接支付给服务商。主机设置属于一次性收费服务。`

#### 4. Do you offer monthly maintenance? / 你们提供每月维护服务吗？

- English: `No recurring maintenance plan is included. If you need an update after launch, request it and we will provide a one-off quote or hourly estimate before starting.`
- Chinese: `我们不提供标准的每月维护配套。网站上线后如需更新，可以提出需求，我们会在开始前提供一次性报价或小时估算。`

#### 5. How many revisions are included? / 包含多少次修改？

- English: `The Basic Website and Editable Website packages include two reasonable revision rounds. Extra revisions or new features are quoted separately.`
- Chinese: `基础网站和可编辑网站配套包含两轮合理修改。额外修改或新功能需要另行报价。`

#### 6. Who provides the content? / 谁提供网站内容？

- English: `The client normally provides the business text, logo, images, and product information. Copywriting or content preparation can be added for an additional fee.`
- Chinese: `通常由客户提供网站文字、标志、图片和产品资料。如需文案或内容整理，可以额外付费委托。`

#### 7. Can you build an online store? / 你们可以制作网店吗？

- English: `Yes. Payment, checkout, inventory, delivery, and customer accounts are custom features and are quoted based on requirements.`
- Chinese: `可以。支付、结账、库存、配送和客户账户属于定制功能，需要根据需求报价。`

#### 8. How do payments work? / 付款方式是怎样的？

- English: `Most projects use 50% before work starts, 30% at an agreed milestone, and 20% before launch. Smaller projects may use 50% before work and 50% before launch.`
- Chinese: `大多数项目采用 50% 开工前付款、30% 里程碑付款、20% 上线前付款。较小项目可以采用 50% 开工前和 50% 上线前付款。`

#### 9. Can you build a mobile app? / 你们可以制作手机应用吗？

- English: `Our main service focuses on websites and web applications. A mobile-friendly web app can be included in a Custom Build. Native mobile apps require separate planning and quotation.`
- Chinese: `我们的主要服务是网站和网页应用。响应式网页应用可以纳入定制开发项目。原生手机应用需要另外规划和报价。`

## 7. Contact page

### URL

`/contact`

### SEO metadata

English:

- **Title:** Contact YJ Studio for a Website Quote
- **Description:** Contact YJ Studio to discuss a Basic Website, Editable Website, hosting setup, or Custom Build.

Chinese:

- **Title:** 联系 YJ Studio 获取网站报价
- **Description:** 联系 YJ Studio，咨询基础网站、可编辑网站、主机设置或定制开发。

### Hero

English:

> Tell us what you want to build.

> Share a few details about your business or idea. We will recommend the most suitable starting point.

Chinese:

> 告诉我们您想打造什么。

> 分享您的业务或想法，我们会为您推荐合适的起点。

### Direct contact buttons

- English: **Message Us on WhatsApp** / **Send Us an Email**
- Chinese: **通过 WhatsApp 联系** / **发送电子邮件**

Replace:

- WhatsApp: `[YOUR WHATSAPP LINK]`
- Email: `[YOUR EMAIL ADDRESS]`

### Enquiry fields

Show the form labels according to the selected language:

| English | 中文 |
|---|---|
| Name | 姓名 |
| Business or project name | 企业或项目名称 |
| Email or WhatsApp number | 电邮或 WhatsApp 联系方式 |
| Package interested in | 感兴趣的配套 |
| What does the website need to do? | 网站需要实现什么功能？ |
| Do you need hosting setup assistance? | 是否需要主机设置协助？ |
| Desired launch date | 期望上线日期 |
| Budget range | 预算范围 |
| Additional details | 其他资料 |
| Send enquiry | 发送咨询 |

Suggested package options:

- Basic Website / 基础网站
- Editable Website / 可编辑网站
- Custom Build / 定制开发
- Not sure yet / 还不确定

### Static-site form note

GitHub Pages cannot process a normal server-side form by itself. Use one of these approaches:

1. WhatsApp and email buttons only.
2. A third-party form service.
3. A form connected to a separate backend or serverless endpoint.

Do not place email passwords, database passwords, API keys, or private credentials in the React repository.

### Success and error messages

- English success: `Thank you. Your enquiry has been received. We will contact you soon.`
- Chinese success: `谢谢！我们已收到您的咨询，很快会与您联系。`
- English error: `Something went wrong. Please try WhatsApp or email instead.`
- Chinese error: `提交失败。请改用 WhatsApp 或电子邮件联系我们。`

## 8. Technical requirements for GitHub Pages

- Build the marketing site as a React static build.
- Keep this public marketing website separate from the Editable Website admin system.
- Configure the React base path correctly if the site is hosted at `username.github.io/repository-name`.
- Use a GitHub Actions workflow to build and publish the site.
- Use client-side routing only if GitHub Pages fallback handling is configured; otherwise use hash routing or simple section links.
- Add a custom domain later if desired and configure HTTPS.
- Optimise images before committing them.
- Test both languages on mobile, tablet, and desktop.
- Check that Chinese characters use a suitable web font and do not overflow buttons or cards.
- Add `lang="en"` or `lang="zh-CN"` to the document according to the selected language.
- Update the page title and meta description when the language changes.

## 9. Launch checklist

- [x] Use Simplified Chinese (`zh-CN`).
- [ ] Add the real business logo and name.
- [ ] Replace WhatsApp and email placeholders.
- [ ] Add the Basic Website demo URL.
- [ ] Add the Editable Website demo URL.
- [ ] Confirm all package prices and scope.
- [ ] Translate and review every visible string.
- [ ] Test the language switcher and saved language preference.
- [ ] Test Home, Custom Build, FAQ, and Contact navigation.
- [ ] Test WhatsApp and email buttons in both languages.
- [ ] Test the GitHub Pages production build.
- [ ] Check mobile layout, Chinese text wrapping, and page speed.
- [ ] Add a privacy policy if analytics or third-party forms are used.
