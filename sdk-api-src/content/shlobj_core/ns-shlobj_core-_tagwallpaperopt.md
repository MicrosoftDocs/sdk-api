---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _tagWALLPAPEROPT structure


## -description


Contains the wallpaper display options. Used with members of the <a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a> interface.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of this <b>WALLPAPEROPT</b> structure.


### -field dwStyle

Type: <b>DWORD</b>

The wallpaper style; one of the following values:



#### WPSTYLE_CENTER (0x0)

0x0. Center the wallpaper image in its original size, filling the remaining area with a solid background color if image is smaller than screen or cropping image if image is larger.



#### WPSTYLE_TILE (0x1)

0x1. Tile the wallpaper image, starting in the upper left corner of the screen. This uses the image in its original size.



#### WPSTYLE_STRETCH (0x2)

0x2. Stretch the image to cover the full screen. This can result in distortion of the image as the image's aspect ratio is not retained.



#### WPSTYLE_KEEPASPECT (0x3)

0x3. <b>Introduced in Windows 7</b>. Enlarge or shrink the image to fill the screen, retaining the aspect ratio of the original image. If necessary, the image is padded either on the top and bottom or on the right and left with the background color to fill any screen area not covered by the image.



#### WPSTYLE_CROPTOFIT (0x4)

0x4. <b>Introduced in Windows 7</b>. Enlarge or shrink the image to fill the screen, retaining the aspect ratio of the original image. If necessary, the image is cropped either on the top and bottom or on the left and right as necessary to fit the screen.



#### WPSTYLE_SPAN (0x5)

0x5. <b>Introduced in Windows 8</b>. Spans the wallpaper across multiple monitors. When this value is set, the <b>WPSTYLE_MAX</b> value must also be set.



#### WPSTYLE_MAX

The maximum legitimate value of these flags, used for validation purposes.

