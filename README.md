## Adding devices

To add new devices you need to modify [devices.json](devices.json) file in `root` directory. *Follow the data scheme or the website may break!*

**devices.json data scheme**

*Last entry must not have a comma after it*

```javascript
[
  {
    "name": "OnePlus 3 / 3T", // Device display name
    "brand": "OnePlus", // Brand, can be ommited
    "codename": "oneplus3", // Codename, this is very important
    "latest_version": "9.0 Pie", // Latest version
    "maintainer_name": "Mr. Stark" // Maintainer name
  }, 
  //..
]
```

To add new builds for devices, you have to go to `/devices/` directory and edit file which name is the *codename* of the device + .json, eg `/devices/oneplus3.json`. *Follow the data scheme or the website may break!*

**Device builds data scheme**

*Last entry must not have a comma after it*

```javascript
[
  {
    "filename": "download-asset-1", // Name of the file to display
    "url": "https://example.com", // Download URL
    "size": "11111111", // Size of the file in bytes, can be ommited
    "date": "2019-05-25T16:40:37.858Z", // Date of publishing, can be ommited, must be valid for JavaScript's Date()
    "changelog": [ // List of changes, can be ommited
      "Added a",
      "Fixed b"
      //..
    ]
  },
  //..
]
```
