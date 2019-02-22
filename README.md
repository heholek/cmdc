<a target="_blank" href="https://chrome.google.com/webstore/detail/chrome-managed-data-clean/anfhmiaflneaeffhlmbcedfjakdlpleg"><img alt="Try it now" src="https://github.com/jay0lee/cros-info/raw/master/cws.png" title="Click here to install this sample from the Chrome Web Store"></img></a>

# Chrome Managed Data Cleanup
  Chrome Managed Data Cleanup (CMDC) is a Chrome extension which aids admins in bulk user Chrome data cleanup. How often have you told users to "delete your cache and cookies" in order to resolve a browser issue? CMDC automates the cleanup process for your users. Admins can automatically empty users cache, history and cookie data. To use CMDC, an administrator must force install the extension for users and configure the app policy.

# Getting started
1. It's recommended that you figure out the *minimal* amount of data that needs to be removed in order to solve the issue. For example, the extension could fix the problem by deleting all user cookies but losing all web settings and logins will be frustrating to your users and it's a sledgehammer approach. You may be able to fix the problem by only [deleting the specific problematic cookie from one website](https://support.google.com/chrome/answer/95647). It's best to try [deleting browser data](https://support.google.com/chrome/answer/2392709) for a few test users interactively to determine exactly what data you need to remove to solve the issue.
1. Now manually install the extension for one user. This will be used to configure the policy that will be set for all users. After install, click the extension broom icon and choose "Options".
1. There are 3 categories of data CMDC can clear: general data, specific cookies and specific history. Check the box for each of these areas you wish to clear. Clearing history and cookies via the general data setting globally removes all of those items based on the time set while using the specific history/cookies setting allows a finer grained approached based on name, site, etc.
1. Once you've configured the options as desired, click the "Download policy" button to save a copy of the resultant policy to disk. You'll need this later to set the policy for all users. You can learn more about [the policy file format in the wiki](https://github.com/jay0lee/cmdc/wiki/Policy-Config).
1. CMDC is meant to be force installed for managed Chrome users. You can force install extensions from the [Google admin console](https://support.google.com/chrome/a/answer/2657289#preinstall) or from managed [Windows](https://support.google.com/chrome/a/answer/7532015), [Macos](https://support.google.com/chrome/a/answer/7517624) and [Linux](https://support.google.com/chrome/a/answer/7517525) devices. CMDC does not work if it wasn't force installed.
1. After force installing the extension, you need to [set policy for the extension](https://support.google.com/chrome/a/answer/6177447?hl=en#custom). The policy tells the extension what data you wish to cleanup. Upload the policy file you generated from the Options page above.
1. The extension will clear user data based on install and then again any time it detects the extension policy has been updated / changed. Outside of these times, the extension should be inactive and not using any system resources.
