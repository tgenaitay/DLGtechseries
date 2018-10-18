### Student Challenge 1: Making a Map For a Landing Page

1. Sign up for API account with your phone number
  - Tencent Developer:  (https://lbs.qq.com)
2. Complete user profile (name is required)
3. Copy the Api Key: [(key管理)](https://lbs.qq.com/console/mykey.html)
  - Looks like (fake, do not use this): OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77
  - [ 创建新密钥](https://lbs.qq.com/console/key.html) if no key is present
    - put in any name in Key名称: e.g. map 
    - ![image-20181019223330397](/Users/dounanhu/Code/wg/DLGtechseries/images/image-20181019223330397.png)
4. Open Tencent static map documentation
  - Documentation: https://lbs.qq.com/static_v2/guide-getImage.html
5. Create basic map
   - Goto section: [图标（markers)](https://lbs.qq.com/static_v2/guide-getImage.html#link-eight) 
   - Copy the URL from the example in the above section:
   - `https://apis.map.qq.com/ws/staticmap/v2/
   ?center=39.908823,116.397496
   &zoom=10
   &markers=color:blue|label:A|39.908823,116.397496
   &key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77
   &size=300*200`
   - Replace the `&key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77` with `&key=YOUR_OWN_KEY` where `YOUR_OWN_KEY` is the Api Key copied in step 3.
     - NOTE: the `&[configuration]=[value]` pattern in the URL -  changing these configurations determines your map's style and the data displayed
   - Paste your URL configured with your own key into your browser's address bar - where the website address usually is.
6. Open Tencent location search documentation 
  - Documentation: https://lbs.qq.com/webservice_v1/guide-search.html
7. Use search API to search for a term (e.g. "NakedHub") to show geolocation data of multiple locations)
  - `https://apis.map.qq.com/ws/place/v1/search?keyword=裸心社naked Hub&boundary=nearby(31.21979,121.44377,1000)&key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77`
    - Replace the `&key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77` with `&key=YOUR_OWN_KEY` where `YOUR_OWN_KEY` is the Api Key copied in step 3. 
8. Add these locations as new markers to your map, following example like this:
  - `https://apis.map.qq.com/ws/staticmap/v2/
  ?center=39.908823,116.397496
  &zoom=15
  &markers=color:blue|label:A|39.908823,116.397496
  &markers=color:yellow|label:B|39.907823,116.397496
  &markers=color:red|label:C|39.907823,116.396496
  &key=OB4BZ-D4W3U-B7VVO-4PJWW-6TKDJ-WPB77
  &size=517*398`
    - Use the latitude (lat) and longitude (long) of your locations to replace those of your marker values (e.g. 39.908823,116.397496 )
9. Change the size, zoom, color, and label values to what you like
10. Open up a mockup landing page (Codepen) 
  - https://codepen.io/anon/pen/WazgZp?editors=1000
  - http://jsrun.net/dwhKp/edit (alternate China version)
  - Click on Fork to Save Your Own Copy - DO NOT EDIT IN PLACE
11. Add the map to the landing page by inserting the URL from step 8 into the <img src=""> tag under the label "MAP GOES HERE" like:
   - `<img src="https://apis.map.qq.com/ws/staticmap/v2/...">`

