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

# WICPngBkgdProperties enumeration


## -description


Specifies the Portable Network Graphics (PNG) background (bKGD) chunk metadata properties.


## -enum-fields




### -field WICPngBkgdBackgroundColor

Indicates the background color. There are three possible types, depending on the image's pixel format.





#### VT_UI1

Specifies the index of the background color in an image with an indexed pixel format.



#### VT_UI2

Specifies the background color in a grayscale image.



#### VT_VECTOR|VT_UI2

Specifies the background color in an RGB image as three USHORT values: {0x<i>RRRR</i>, 0x<i>GGGG</i>, 0x<i>BBBB</i>}.


### -field WICPngBkgdProperties_FORCE_DWORD



