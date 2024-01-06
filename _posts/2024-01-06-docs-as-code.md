---
author: craig
title: "Docs-as-Code Tooling: A Comparison"
category: technical-writing
tags: api-documentation docs-as-code
---

<figure class="aligncenter">
	<img src="/assets/images/printing.png" width="800" height="300" alt="Artist visualization of Johannes Gutenberg in his workshop, showing his first proof sheet." />
</figure>

With the range of software documentation tools available it's difficult to know where to start. 

As part of a course, I recently compared available documentation tools to determine which are best suited for a project I've been working on. What follows is a summary drawing from my own practical experience working as a technical writer while considering perspectives of others working in the field.

<!--more-->

## Summary Video

<iframe width="560" height="415" src="https://www.youtube.com/embed/3zCv6eEK_Vo?si=q6ceT_l0PEW1-D85" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Background: Software Documentation & Tooling 

Software products require technical documentation for users. For many SaaS companies, effective API documentation is essential for growth as it enables external developers and third parties to implement solutions independently without relying on internal development resources while minimizing support through training and customer service.

Authoring tools are generally used to create and publish documentation as web applications. The general minimum requirements for such tools include:
internationalization (i18n), code samples in various languages, version control, and generation from OpenAPI specifications. Effective documentation authoring applications should foster a positive user experience for all stakeholders. Support for the addition of video content or interactive elements is often an added benefit.

There are various open source solutions for new authoring tools including Markdoc, Nextra, Gatsby, MkDocs, and more. The ideal solution is easy to use, visually appealing, adaptable, and meets all the minimum requirements of the organization and its users. Amid the range of choices, companies often struggle choosing a documentation tool that is fit-for-purpose.

## Docs-As-Code

Docs-as-code means "writing, testing, publishing, and maintaining documentation using the same tools developers use for software code" [1]. With docs-as-code, documentation is managed in the same way as software code. This involves the following:

- Writing content with markdown files in an IDE.
- Version control system to store and version it.
- Automated testing.
- Build and deploy system.

Creating documentation is a multiphase process that involves identifying user needs, creating a plan, drafting, editing, and publishing content [3]. Although the tool directly touches on the latter three (drafting through to publishing), it is the central element throughout. The tool impacts essential non-tangible aspects such as user/employee satisfaction and quality perceptions.

<figure class="center" style="margin-top: 2rem;margin-bottom:2rem;">
	<img src="/assets/images/docs-as-code-flow.png" width="800" alt="Poster for docs-as-code" style="margin:auto;" />
	<figcaption style="text-align:center;">Docs-as-code workflow. Source: <a target="_blank" href="https://www.doctave.com/blog/2021/08/30/why-you-should-consider-docs-as-code.html">Docave</a>.</figcaption>
  
</figure>

## Tooling

Several options for documentation tooling exist. They differ based on the following:

- Tech stack and development frameworks used.
- Features and plugins.
- Starter repos and ease of set up.

I compared eight tools that are widely used in industry. The eight were narrowed down from web research. For each tool, approximately 1-2 hours was spent
conducting a feasibility trial consisting of the following steps:

1. Reading the website to determine background information, technical overview, and available resources.
2. Downloading/developing a starter repository that includes all the minimum requirements: internationalization, code samples in various languages, version control, and OpenAPI specifications.
3. Adding markdown content and custom styling. During the process, a qualitative assessment was conducted (using note taking), outlining what went well, challenges, and roadblocks. Table 1 below provides a summary of the tools with advantages and disadvantages of each.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;line-height:normal;}
.tg .tg-jgcz{border-color:inherit;color:#555;text-align:left;vertical-align:middle;line-height:normal;}
.tg .tg-uzvj{border-color:inherit;font-weight:bold;text-align:center;vertical-align:middle;line-height:normal;}
.tg .tg-0mtp{border-color:inherit;color:#555;text-align:left;text-decoration:underline;vertical-align:top;line-height:normal;}
</style>

#### Tool Comparison
<table class="tg">
<thead>
  <tr>
    <th class="tg-uzvj">Tool</th>
    <th class="tg-uzvj">Description</th>
    <th class="tg-uzvj">Advantages</th>
    <th class="tg-uzvj">Disadvantages</th>
    <th class="tg-uzvj">Live Example</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-jgcz">Markdoc</td>
    <td class="tg-jgcz">Open sourced by Stripe in<br>2022. Integration with<br>framework of choice: Next.js,<br>React</td>
    <td class="tg-jgcz">- Newly released and widely used<br>- Extensible and customizable</td>
    <td class="tg-jgcz">- Set up and default starter<br>repos not as straightforward as other<br>tools</td>
    <td class="tg-0mtp"><a target="_blank" href="https://stripe.com/docs"><span style="color:var(--main-color)">stripe.com/docs</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">Docusaurus</td>
    <td class="tg-jgcz">Open sourced by Facebook in<br>2017. MDX based. React +<br>Node static site generator.<br>Angolia for search and<br>Crowdin for translations.<br>Versioning support.</td>
    <td class="tg-jgcz">- Quick setup: starter templates /<br>easy to get started<br>- Regular product releases<br>- Widely used<br>- Lots of features &amp; plugins<br>available</td>
    <td class="tg-jgcz">- Limited to React<br>- No built in feedback<br>component<br>- Plugin integration not<br>always straightforward</td>
    <td class="tg-0mtp"><a target="_blank" href="https://reactnative.dev/"><span style="color:var(--main-color)">reactnative.dev</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">Nuxt Content</td>
    <td class="tg-jgcz">Module that provides a<br>file-based layer to Nuxt stack.<br>Based on Vue components</td>
    <td class="tg-jgcz">- Widely used; built/maintained by<br>Nuxt Core team</td>
    <td class="tg-jgcz">- Setup not as quick as<br>Docusaurus</td>
    <td class="tg-0mtp"><a target="_blank" href="https://nuxtdoc.js.org/"><span style="color:var(--main-color)">nuxtdoc.js.org</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">Netra</td>
    <td class="tg-jgcz">From Next.js creators in 2020.<br>Based on MDX.</td>
    <td class="tg-jgcz">- Syntax highlighting, i18n creation,<br>out-of-the-box text search</td>
    <td class="tg-jgcz">- Less featured than some<br>others (e.g., Docusaurus)</td>
    <td class="tg-0mtp"><a target="_blank" href="https://turbo.build/repo/docs"><span style="color:var(--main-color)">turbo.build/repo/docs</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">VuePress</td>
    <td class="tg-jgcz">Vue-powered static site<br>generator.</td>
    <td class="tg-jgcz">- Default theme for quick setup<br>- Ability to use Vue inside md files<br>(for dynamic content)</td>
    <td class="tg-jgcz">- Not updated as often asthose from larger orgs<br>(Markdoc, Docusaurus)</td>
    <td class="tg-0mtp"><a target="_blank" href="https://v2.vuepress.vuejs.org/guide/getting-started.html"><span style="color:var(--main-color)">v2.vuepress.vuejs.org</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">MkDocs</td>
    <td class="tg-jgcz">Popular Python SSG. YAML<br>file configuration.</td>
    <td class="tg-jgcz">- Available themes for quick setup<br>- Easy to customize</td>
    <td class="tg-jgcz">- Not a SPA</td>
    <td class="tg-0mtp"><a target="_blank" href="https://squidfunk.github.io/mkdocs-material/getting-started/"><span style="color:var(--main-color)">squidfunk.github.io</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">Docsify</td>
    <td class="tg-jgcz">Vue compatible SSG</td>
    <td class="tg-jgcz">- Lightweight<br>- Plugins</td>
    <td class="tg-jgcz">- Not a SPA<br>- Templates / themes are<br>minimal</td>
    <td class="tg-0mtp"><a target="_blank" href="https://docsify.js.org/#/"><span style="color:var(--main-color)">docsify.js.org</span></a></td>
  </tr>
  <tr>
    <td class="tg-jgcz">Gitbook</td>
    <td class="tg-jgcz">Documentation platform</td>
    <td class="tg-jgcz">- Widely used<br>- PDF support<br>- Rich Plugin system<br>- Content editor for authoring</td>
    <td class="tg-jgcz">- Shifting from open source<br>to product<br>- Only free for open-source<br>teams</td>
    <td class="tg-0mtp"><a target="_blank" href="https://docs.gitbook.com/"><span style="color:var(--main-color)">docs.gitbook.com</span></a></td>
  </tr>
</tbody>
</table>


#### Rating 

Each tool was given a rating from 0-4 based on criteria which included the following:

- Tech stack that is a fit for internal tech teams.
- Features and plugins.
- Ease of use and setup.
- Whether it's a maintained project in relatively wide use.

One additional requirement is that the tooling is maintained as an ongoing project that is widely used in the industry. A maintained, widely adopted project allows for technical support, sharing best practices, and regular updates.

Below are the ratings assigned to each tool.

<style type="text/css">
table  {border-collapse:collapse;border-spacing:0;}
table td{border-color:black;border-style:solid;border-width:0px;
  overflow:hidden;padding:5px 5px;word-break:normal;}
</style>

<table>
  <tr>
    <td>Markdoc</td>
    <td>&starf;&starf;&starf;&star;</td>
  </tr>
  <tr>
    <td>Docusaurus </td>
    <td>&starf;&starf;&starf;&starf;</td>
  </tr>
  <tr>
    <td>Nuxt Content</td>
    <td>&starf;&starf;&starf;&starf;</td>
  </tr>
  <tr>
    <td>Nextra</td>
    <td>&starf;&starf;&starf;&star;</td>
  </tr>
  <tr>
    <td>VuePress</td>
    <td>&starf;&starf;&starf;&star;</td>
  </tr>
  <tr>
    <td>MkDocs</td>
    <td>&starf;&starf;&star;&star;</td>
  </tr>
  <tr>
    <td>Docsify</td>
    <td>&starf;&starf;&star;&star;</td>
  </tr>
  <tr>
    <td>GitBook</td>
    <td>&starf;&star;&star;&star;</td>
  </tr>
</table>

Based on the rating, Docusaurus and Nuxt Content were deemed the best suited. These tools are based on React and Vue, respectively, and offer an option based on the preferred framework of the team.

## Conclusion

Organizations often struggle finding the right tool for their documentation. This feasibility report assessed eight different tools to be used in a docs-as-code workflow for a SaaS company. Each tool was tested against the minimum requirements and the advantages/disadvantages of each was noted. A rating of 0-4 was assigned to each. Two tools, Docusaurus and Nuxt Content came out with the highest ratings.

For the given context Docusaurus is recommended as a documentation tool. Docusaurus offers easy set up and is based on React, which is used by the team. As a maintained, open source framework, Docusaurus also offers updates and resources.

## References

[1] R. Krátký, 'DevOps meets Docs: Documentation as Code', OSSummit Europe, 2018.
[Online]. Available: <a target="_blank" href="https://events19.linuxfoundation.org/wp-content/uploads/2017/12/DevOps-Meets-Docs-Docume
ntation-as-Code-Robert-Kratky-Red-Hat.pdf">https://events19.linuxfoundation.org/wp-content/uploads/2017/12/DevOps-Meets-Docs-Docume
ntation-as-Code-Robert-Kratky-Red-Hat.pdf</a>

[2] E. Holscher. “Docs as Code”. Docs as Code. <a target="_blank" href="https://www.writethedocs.org/">https://www.writethedocs.org/</a> (accessed Aug 1, 2023).

[3] J. Bhatti, Z.S. Corleissen, J. Lambourne, D. Nunez, and H. Waterhouse, Docs for Developers: An Engineer’s Field Guide to Technical Writing. Berkeley, CA: Apress, 2021.

[4] G. Bine, ‘Docs as Code and DITA’, TCUK, 2019. [Online]. Available: <a target="_blank" href="https://istc.org.uk/wp-content/uploads/2021/11/George-Bina-%E2%80%93-Docs-as-Code-and-DITA.pdf">https://istc.org.uk/wp-content/uploads/2021/11/George-Bina-%E2%80%93-Docs-as-Code-and-DITA.pdf</a>

[5] Begley, Niklas. “Why you should consider using docs-as-code”. Docave. <a target="_blank" href="https://www.doctave.com/blog/2021/08/30/why-you-should-consider-docs-as-code.html">https://www.doctave.com/blog/2021/08/30/why-you-should-consider-docs-as-code.html</a> (accessed Jul 15, 2023).

[6] NuxtJS. “Content made easy for Vue Developers”. NuxtJS. <a target="_blank" href="https://content.nuxtjs.org/">https://content.nuxtjs.org/</a> (accessed Jul 15, 2023).

[7] Meta Platforms, Inc. “Docs.” Docusaurus. <a target="_blank" href="https://docusaurus.io/">https://docusaurus.io/</a> (accessed Aug 1, 2023).