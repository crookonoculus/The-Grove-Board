# The Grove Board

Independent image feed for **The Grove Github Bull** quad in the LSVR **The Grove** scene. This repository does not change the other worlds' shared event boards.

## Update the board

1. Upload PNG or JPG images into this repository. The supplied Grove ads are in `adsforgrove_`; the two posters copied from the old feed are in `images/existing`.
2. Edit `events.json` and add each image's relative path to the `monthly` array. Array order is the display order. The name `monthly` is required by the existing Unity component; it does not restrict images to a calendar month.
3. Commit the changes. Images rotate every four seconds with the existing Unity settings. The board downloads the feed when enabled or when entering the world; an already-open world does not continuously refresh the feed. GitHub caches may take a few minutes to refresh.

Use valid JSON: double quotes, commas between entries, no trailing commas. Uploading an image alone does not add it to the rotation: its path must appear in `monthly`. Remove a path from `monthly` to stop displaying that image.

Feed: https://raw.githubusercontent.com/crookonoculus/The-Grove-Board/main/events.json

This repository is public so Quest clients can fetch it without credentials. A new app build is needed once to install the new board URL. After that, image/feed updates here do not require a new APK.
