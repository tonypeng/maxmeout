# maxmeout
Monitor your nearby Apple stores for Airpods Max availability!

<p align="center">
  <img src="https://github.com/tonypeng/maxmeout/raw/main/assets/running_screenshot.png" />
</p>

### Instructions
By using this software, you agree to the terms in the `LICENSE` file.
1. First, you'll need to get the page URL of the store you want to monitor (the script will automatically monitor (up to) the 11 nearest stores to that store as well). To do that, go to the page on the Apple website for your store (you can just google "apple \<location\>") and copy the URL. For example, the Apple Park Visitor Center store page is https://www.apple.com/retail/appleparkvisitorcenter/.
2. Install the dependencies for the code. There are two: `requests` for fetching inventory data from Apple's website and `beepy` for making a beep sound when inventory is found.<br>`$ pip3 install requests beepy`
3. Now you're ready to run the script! Download this repository, open a terminal window, and `cd` to where you've downloaded the code. This should be the same directory where `main.py` is. Run the script with:<br><br>```$ python3 main.py --store_url STORE_URL --models MODELS_TO_WATCH```<br><br>replacing `STORE_URL` with the store page url you noted down in step 1, and `MODELS_TO_WATCH` with a comma separated of the list of colors you want to monitor: `space_gray`, `silver`, `green`, `sky_blue`, `pink`.<br><br>For example, to monitor for space gray, silver, and sky blue availability at Apple Park Visitor Center:<br>`$ python3 main.py --store_url https://www.apple.com/retail/appleparkvisitorcenter/ --models space_gray,silver,sky_blue`<br>At the time of writing, `silver` is in stock at Apple Park Visitor Center. The script will keep repeatedly checking until you terminate it, so now get back to doing whatever you were doing before! If it finds inventory, it'll let you know with a sound.

Good luck, and happy hunting!
