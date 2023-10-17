# YouTube iFrame AdBlocker

## Description

"YouTube iFrame Bypass" is an ingenious userscript that helps persistent YouTube viewers bypass the frustrating "Ad blockers are not allowed on YouTube" message. It employs a clever technique of dynamically inserting an `iframe` player to replace the standard YouTube player. This method effectively circumvents YouTube's ad-blocker detection, allowing for an uninterrupted, ad-free viewing experience even after YouTube's standard measures have been triggered. Ideal for those who have been directly targeted by the anti-adblocker prompt and do not wish to disable their ad blockers or subscribe to YouTube Premium.

## How YouTube iFrame AdBlocker Works

When YouTube detects an ad blocker, it sometimes displays a message enforcing ad viewing. This script counters that by employing the following strategy:

1. **Detection:**
   It continuously monitors the YouTube page for any changes that indicate the presence of an enforcement message (triggered by ad-blocker detection). This is done using a web API called `MutationObserver`, which can detect when specific elements are added to the webpage.

2. **iFrame Replacement:**
   Upon detecting the enforcement message, the script dynamically creates an `iframe` element configured to embed the currently viewed YouTube video. The `iframe` uses a URL that includes the video ID (extracted from the current page's URL) and an autoplay parameter.

3. **Autoplay Handling:**
   The script incorporates an autoplay feature, allowing users to automatically move to the next video after the current one ends. This is managed through a custom control within the `iframe` and the browser's local storage, which remembers if the user has the feature enabled.

4. **End of Video Detection:**
   To facilitate autoplay, the script also monitors for the end of a video, waiting for the UI changes that signal this event. If autoplay is active, it then initiates the next video.

Please note that this approach is a workaround and relies on current YouTube's page structure and behavior, which may change, potentially breaking the script's functionality.

## Prerequisites

Before you begin, ensure you have met the following requirements:
* You have a modern web browser.
* You have installed a userscript manager, such as Tampermonkey or Greasemonkey.
* You have encountered the "Ad blockers are not allowed on YouTube" message on YouTube.

## Installing YouTube iFrame AdBlocker

To install the YouTube iFrame AdBlocker, follow these steps:
1. Open your userscript manager's dashboard.
2. Go to the 'Utilities' section.
3. Under 'URL', paste the link to the raw `.user.js` file, then click 'Import'.
4. Once the script is imported, you'll be redirected to the script installation page. Click 'Install' to proceed.

Alternatively, you can create a new script in your userscript manager and copy-paste the code.

## Using YouTube iFrame AdBlocker

After installation, the script should work automatically when you navigate to YouTube, specifically when the "Ad blockers are not allowed on YouTube" message has been displayed. Videos should load in an embedded iFrame, preventing YouTube's anti-adblock system from detecting the adblocker.

Please note that this script won't remove ads shown by the video content creators themselves and is intended to work after YouTube's anti-adblock message has been encountered.

## Contact

If you want to contact me, you can reach me on Discord as jordanro2.

## License

This project uses the MIT License. See [LICENSE](LICENSE) for details.

## Disclaimer

This script is created for educational purposes and personal use only. Circumventing ad display can violate YouTube's terms of service. Please be aware of the potential consequences, including account suspension or legal action, before using the script. The author does not accept any responsibility for any repercussions that occur from using this script.
