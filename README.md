<a name="banner" href="#banner">![banner](/images/banner.png)</a>

[![HitCount](https://hits.dwyl.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page.svg?style=flat)](http://hits.dwyl.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page) [![Pull Requests welcome](https://img.shields.io/badge/PRs-welcome-ff69b4.svg?style=flat-square)](https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22) <a href="https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page/pulls"><img src="https://img.shields.io/github/last-commit/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page?style=flat-square"></a> <a href="https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page/graphs/contributors"><img src="https://img.shields.io/github/contributors/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Experience-Page?style=flat-square"></a> <a href="https://invite.sndevs.com"><img src="https://img.shields.io/badge/community-sndevs-630330?style=flat-square"></a> 
# Welcome!
Hola! @MGOPW here. This Experience Page repository has a [sister repository](https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Custom-Component) containing the accompanying Custom Component for this page, be sure to check out both repos to get the full picture of what we are doing here. This is a bit complex of a setup, but it should provide you with a great starting point to learn Custom Components and UI Builder. **You must check out the [Installation instructions](#installation-instructions) section for more information on how to install these!**

Other resources you should check out:
- [Next Experience Center of Excellence](https://www.servicenow.com/community/next-experience-articles/next-experience-center-of-excellence/ta-p/2332092) - This is the main place where we post Next Experience, Workspace, and UI Builder enablement materials.
- [You & I Builder Live](https://www.youtube.com/playlist?list=PL3rNcyAiDYK2Bgzj4mRdtfxMpGkI5KXBJ) - A more technical and in-depth view in to UI Builder packaged in a hilarious and casual format. Come hang out in chat and learn some UI Builder while you're at it!
- [Next Experience Academy](https://www.servicenow.com/community/next-experience-blog/next-experience-academy-upcoming-and-recorded-sessions/ba-p/2272673) - Monthly webinar series we host for all audiences, all academies are uploaded to [this youtube playlist](https://www.youtube.com/watch?v=wuli92FRGC0&list=PLkGSnjw5y2U6hmEPcDcJ53FHwKJIvoLvr) after the fact.

And lastly, this repository is part of a larger coordinated effort by the ServiceNow Developer Advocate to provide lots of fun ServiceNow projects for Hacktoberfest. Be sure to check out the [main repository README](https://github.com/ServiceNowDevProgram/Hacktoberfest) to see what else you can participate in!
 
# Content
- [What is this even for?](#what-is-this-even-for)
- [What do i need to know?](#what-do-i-need-to-know)
- [Information on Portal Experience menus](#some-information-on-portal-experience-menus)
- [Installation Instructions](#installation-instructions)
# What is this even for?
You can create something called Portal Experiences in UI Builder, which are similar to Workspaces. They aren't currently a replacement for Angular Service Portal as of the writing of this repo, you can read more about this [on the Next Experience Community forum](https://www.servicenow.com/community/next-experience-articles/portal-experience-faqs/ta-p/2331979). These Portal Experiences have menus that are generated from JSON, and it's a pain to manage them right now. So Jesalyn and I decided to do something fun - why not learn how to make a custom component while simultaneously spending hundreds of hours making a solution for something that only mildly inconvenienced us? (And then submit it as a Creator Con lab!)

And that's what you see here! We've created a Custom Component and Experience page combo to make menus for us. We didn't quite finish it, but we wanted to share the source code with everyone so you'd have a good starting point to look at when building your own custom components. 

But thanks to Hacktoberfest, it gets even better - now you can help us finish it by contributing! Be sure to check out our [CONTRIBUTING.md]() file for more info on how you can help!

![my dream](/images/design.png)

This is what i pictured the final page would look like. We're almost there! 

# What do I need to know?
- This repository contains the Experience Page that encapsulates the Custom Component from the sister repository. You need to install this to have an easier time testing your own component, all installation instructions are in  [CONTRIBUTING.md](CONTRIBUTING.md).
- We've created issues to list out contribution ideas you might want to pick up! Or if you think of new stuff to contribute, make a new issue and let us know what you're going to work on.
- Design philosophy: Components should be presentational if possible, but if the exchange with the server data is complex enough, and you're going to use it in multiple places, you're really better off with a connected component. In this case, we tried to stick to making the component more presentational in nature so keep that in mind when adding new features if possible.
- Collaborating with others on pages is rather complex due to how the scopes work, so be sure to follow every step in our [CONTRIBUTING.md](CONTRIBUTING.md) so you can be successful and have your PRs approved.
# Some information on Portal Experience menus
I've tried to reverse engineer these as best as I could to make this component, but I know I haven't fully figured it out yet. Here's what I already know to help you get started.

Menus have a complex parent/child relationship that determines their behavior and how menus are presented. [There's an issue created to investigate and implement this feature](https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Custom-Component/issues/1) so if you want to delve deeper, please go right ahead. 

For example, the more menus you have nested, their appearance and layout changes in the menu itself. I don't quite remember the number, unfortunately.

Actions have similar behavior, which I haven't cataloged. Sometimes they show up as buttons, while other times they show up as links. 

![anatomy of a menu](/images/menuanatomy.png)

Visual of what i've figured out so far.


# Installation instructions
Follow these instructions to install the experience page and the menu builder component in your instance.

If you ever get stuck, you can find us over on the [SNDEVS](https://sndevs.com) community ([invite.sndevs.com](https://invite.sndevs.com)) in either the `#hactoberfest` channel or the `#next-experience-uib-workspace` channel. 

Things you'll need:
- A [ServiceNow Developer Instance](https://developer.servicenow.com/)

1. Open App Engine Studio and import this repository directly to your instance.
2. Install the [Update Set provided in the Releases section of the sister repository](https://github.com/ServiceNowDevProgram/Menu-Generating-Operations-Program-Widget-Custom-Component/releases/tag/original).
3. Search for `Hacktober23` in the Filter Navigation 
	1. **Menu Builder** – takes you to the page to play with the component 
	2. **UI Builder** – takes you to the UI Builder page for the Menu Builder page 
