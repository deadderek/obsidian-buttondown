# Obsidian Buttondown Plugin

[Buttondown](https://buttondown.email) is a tool for producing email newsletters. It likes emails written in Markdown, and has an API.

This plugin allows you to write drafts for your emails in [Obsidian](https://obsidian.md), then send them to Buttondown with a single command, ready for you to preview and send.

## How to use

1. Install the plugin through the Obsidian's community plugins browser.
2. Enable the plugin in Obsidian.
3. Fill in your API token in the settings. You can find your token [here](https://buttondown.email/settings/programming) in your Buttondown settings
4. Write an email in an Obsidian note
5. Call the command "Create a new Buttondown draft from this note" from the Command Palette (Ctrl-P) to create a new draft in Buttondown, where the email subject is the filename of your note, and the email body is the content of your note
6. See your drafts in Buttondown [here](https://buttondown.email/emails/drafts), where you can edit and preview the draft, then schedule or send the email to your list.

## Privacy and network usage

This plugin makes network requests to Buttondown's API (`https://api.buttondown.email`) when you use the command to create a draft. The following data is transmitted:

- Your Buttondown API key (configured in settings)
- The content of your note (email body)
- The filename of your note (email subject)
- Any images referenced in your note (uploaded to Buttondown's image storage)

All data is sent directly to Buttondown's servers over HTTPS. No data is collected, stored, or transmitted to any other third parties. The plugin does not include any telemetry or analytics.

You must explicitly invoke the "Create a new Buttondown draft from this note" command for any network requests to occur. The plugin does not transmit data automatically or in the background.

## Support me

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/U6U7BUEZ6)


## How to make a release

- Update `minAppVersion` manually in `manifest.json` if required, then `npm version patch`, `npm version minor` or `npm version major` .
- Create a tag that matches that version `git tag -a 1.0.1 -m "1.0.1" && git push origin 1.0.1`
