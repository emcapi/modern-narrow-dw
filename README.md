# Modern Narrow Light/Dark - Layout for Dreamwidth
A minimalist theme/layout for Dreamwidth inspired by Tumblr and other popular social media sites, prioritizing readability and customization.

<ins>**This code & associated documentation is 100% human-made!</ins> :heart:**

![Small preview image of Modern Narrow Light](./preview%20pics/mnlight-preview-thumbnail.png)
![Thumbnail image of Modern Narrow Dark](./preview%20pics/mndark-preview-thumbnail.png)

For full-sized previews including comment threads, see [preview pics](./preview%20pics) folder.

## Main Features
- Light and dark default theme options.
- Support for **all** standard column layouts!
- Fixed-width main column for better post readability on desktop.
- Full mobile support/compatibility. (Requires Responsive Comments setting enabled; see [Recommended Settings](#recommended-settings).)
- Comment page with thread indicators.
- Designated code section for most hard-coded colors (see [Custom Color Themes](#custom-color-themes)).

## Permissions
See LICENSE.md for full legal permissions.

### License TL;DR:
- You can use/copy/edit/share/etc. this theme as long as you keep the licence + attribution. Go nuts!
- If something's busted, legally speaking, it's not my problem and you can't sue me for it.

### Unofficial perms:
- If you make an edit or theme for this or whatever, let me know! I'd love to see it, and I'll put a link on the emcapi-styles community page.
- If you use this theme, while on-blog credit isn't officially necessary (the legal bit about including the license is more in terms of redistribution/edits, as far as I know), I really appreciate it!

## Installation
From the Dreamwidth home page:
1. Under the Organize menu, pick "Select Journal Style".
2. Search for "plain". This should bring up Plain for Tabula Rasa. Click "apply theme".
3. Scroll down and pick the column setup you want. You will need to remember whether it has 0, 1, or 2 sidebars (will affect recommended settings).
4. At the top of the page, select "Customize Journal Style" from the Organize menu, or "Customize current theme" under the "[user]'s Current Theme" section. These should both bring you to the "Customize Journal Style" page.
5. Under the "Custom CSS" tab, make sure "Use layout's stylesheet(s)" is checked (should already be checked by default).

At this point, you have 2 main options. Don't worry, you can always swap to the other installation type if you change your mind later!

### Option 1: CSS Copy/Paste
#### Choose this if:
- You dislike unexpected UI changes.
- You don't want to deal with possible bugs caused by future changes.
- You would like to make changes to your copy of the theme (e.g. editing or removing hard-coded colors).

#### Instructions for this option (continued from Installation):
6. Open the .css files for either the [light](./Modern%20Narrow%20Light.css) or [dark](./Modern%20Narrow%20Dark.css) theme, and copy all contents.
6.5. (Bonus step!): If you already know the specific changes you want to make,[^1] you can paste the code into a plain-text editor (e.g. Notepad or Notepad++) to edit it before putting it on your journal. (Don't use Microsoft Word or other full-fledged text editors, as they may add weird formatting characters.)
7. Paste your (optionally edited) code into the "Use embedded CSS" box on Dreamwidth.
8. Save changes.
9. Under the "Presentation" tab, configure the [Recommended Settings](#recommended-settings) from the next section.

[^1]: See [Custom Color Themes](#custom-color-themes) and [Other Customization](#other-customization) for tips and ideas.

### Option 2: Stylesheet Link
#### Choose this if:
- You want to keep up-to-date on the latest version, including any future fixes/changes/additions, without having to manually update every time.
- You don't plan on making any changes to the code.

#### Instructions for this option (continued from Installation):
6. Right click and copy the link shown here for either the [light](https://raw.githubusercontent.com/emcapi/modern-narrow-dw/refs/heads/main/Modern%20Narrow%20Light.css) or [dark](https://raw.githubusercontent.com/emcapi/modern-narrow-dw/refs/heads/main/Modern%20Narrow%20Dark.css) theme (should point to raw.githubusercontent.com).
7. Paste link into the "Custom stylesheet URL" box.
8. Save changes.
9. Under the "Presentation" tab, configure the [Recommended Settings](#recommended-settings) from the next section.

## Recommended Settings
(If you have sidebar/s): **"The width at which the layout switches from single column mode (mobile view) to multiple columns if selected (tablet view)"**: Set this to the total width of your sidebars, plus 45em. If you've left the default 15em width, this would be a total of 60em with one sidebar, or 75em with two sidebars.

**"Indentation for nested comment threads"**: Set to "Responsive".

**"Beyond this depth, use compact styling to indicate thread depth (mobile). Ignored for static indentation"**: Set to "4".
While not strictly required, you may want to set the next option (compact styling for desktop) as well, especially if you frequently end up in deep comment threads. 10 is a good starting point.

> [!WARNING]
> If you **don't** configure the indentation style + mobile compact styling settings, you'll get really annoying horizontal scrolling on mobile on any pages with deep comment threads (depth of 5 or more).

### Non-customizable/hardcoded settings:
- Left/right icon button alignment (will do nothing; setting to "none" should still work)
- Left/right "place of icons in entries and comments" (will do nothing; setting to "none" should still work)

If a setting is not listed here, you should be able to configure it as you like. If this results in problems, please open an issue on Github or message me on Dreamwidth (see Bug Reports).

## Custom Color Themes

Part of the goal for this theme is being easy to customize. For that purpose, all hardcoded colors are in a designated section at the start of the code for easy editing. This also means you can swap the entire section out for a different theme if you want!

To make this easier, under the Components folder in this repository, there's a special edition of Modern Narrow called Modern Narrow Core, which has an empty Color section to paste in your own. There's another folder with the standalone default light/dark color themes.

> [!NOTE]
> If you're planning to create your own color theme from scratch, MN Core may be useful to you, but I highly recommend grabbing either the light or dark color settings standalone to start working from. There's tons of things I found that Dreamwidth's default customization settings don't really touch.

### Dreamwidth color settings

Out of the box, MN Light will be compatible with all built-in Dreamwidth color settings except for border and link colors. MN Dark has more limited compatibility, because the default colors need to be hardcoded.

For any colors that can normally be adjusted via DW color settings, you can delete their assignment in the Color section to allow customization via DW. A lot of components get assigned colors in bulk to reduce code length; for these, just delete the specific component you want to change from the assignment list. (Obviously, you can also just set a different hex code there, but this might be inconvenient if you like changing your color scheme often or you want to test out a bunch of different colors.)

To make any code edits, you'll need to use the [CSS Copy/Paste](#option-1-css-copypaste) installation option.

## Other Customization
Again, to make any code edits, you'll need to use the [CSS Copy/Paste](#option-1-css-copypaste) installation option.

### Custom Fonts

Custom fonts won't work by default, but can be easily enabled with a minor code edit. You'll just need to <ins>delete</ins> the following bit of code right after the Colors section, under the `/* FONT TWEAKS */` line:
```
body {
    font-family: sans-serif;
}
```
...and then you can set up your custom font(s) under the Dreamwidth customization settings!

### Remove Header

This is also a pretty easy code edit. <ins>Paste in</ins> the following bit of code at the start (or any blank line) of the layout CSS:
```
#header {
    display: none;
}
```
Look Ma, no header!

(If you have the navigation links module enabled, you might want to make sure it's set to show up in one of the module sections, and not in your header.)

### Default Icon Buttons

If you want the classic Dreamwidth icon buttons back, <ins>delete</ins> everything from right after the `/* CUSTOM ICON BUTTONS */` line to the end of the file.

## Bug Reports

If you run into any problems, despite using the [Recommended Settings](#recommended-settings), please open a Github issue or send me a Dreamwidth message including:

- A quick description of the issue
- A screenshot or screenshot link, if possible
- Your column configuration setting
- A link to the page you were having issues on, if possible
- What browser you're using
- What type of device you're on (phone/tablet/desktop)

I'll take a look and see if I can fix it!

Legal disclaimer: ongoing support is provided at author's discretion, and not guaranteed.

(Also, I *extra* can't guarantee support for edits, though if you send me a message I may be able to help troubleshoot a bit.)

## Bonus storytime
### The real reason I made MN Core (or: the tale of my developer woes)

Yeah so a lot of my motivation for adding a separate version with no colors was... because it made development a lot easier lol.

Originally, I planned to wait until I was happy with the light theme to make a dark theme. Well. I hit a point where I thought I was happy with the light theme. So then I made the dark theme.

And then I found like five million other things I wanted to change, and let me tell you, copy/pasting every single edit I made across two different files was a colossal pain in the ass and got old REAL fast.

Then I realized that having a separate section for as many hardcoded colors as possible was probably a good idea in general, so that's how the old Customization section (which only included colors you could change through Dreamwidth's settings if you deleted them out of the code) got scrapped in favor of the much more comprehensive Color section. And I made the Core edition so that I could load up stylesheets separately and, when I had a version I was finally happy enough with to release, just drop in the light and dark themes and post those.

...Then I also realized I should maybe make an actual Git repository for this, because this whole project got way out of hand. I don't know whether I'll return to this in the future; if I do, it'll be nice to have one place to keep track of changes. If I don't, it'll also be nice to have an easy way for people to keep developing this theme or make their own versions, if they want. Also, it's a good excuse for me to get more practice with Github.

## Credits
Icon font: [Google Material Symbols Rounded](https://fonts.google.com/icons)
