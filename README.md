# Firefox-Mastodon-CSS
Custom CSS for Mastodon advanced view in Firefox.

Based on instructions here: https://superuser.com/questions/318912/how-can-i-override-the-css-of-a-site-in-firefox-with-usercontent-css


1. Open Firefox and press Alt to show the top menu, then click on Help → More Troubleshooting Information
1. Click the Open Folder button beside the Profile Folder entry
1. Create a folder named chrome in the directory that opens
1. In the chrome folder, create a CSS file with the name userContent.css
1. Copy the following code to userContent.css, replacing "mastodon.social" with the Mastodon instance you use.
```
@-moz-document domain(mastodon.social) {
    .column[aria-label="Home"] { width: 600px !important; }
	.media-gallery { max-height: 300px !important; }
}
```
6. Open another tab in Firefox, go to about:config, and set toolkit.legacyUserProfileCustomizations.stylesheets preference to true.
7. Restart Firefox.
