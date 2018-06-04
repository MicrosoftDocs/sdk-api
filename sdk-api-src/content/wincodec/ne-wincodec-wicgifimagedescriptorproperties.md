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

# WICGifImageDescriptorProperties enumeration


## -description


Specifies the image descriptor metadata properties for  Graphics Interchange Format (GIF) frames.


## -enum-fields




### -field WICGifImageDescriptorLeft

[VT_UI2] Indicates the X offset at which to locate this frame within the logical screen.


### -field WICGifImageDescriptorTop

[VT_UI2] Indicates the Y offset at which to locate this frame within the logical screen.


### -field WICGifImageDescriptorWidth

[VT_UI2] Indicates width of this frame, in pixels.


### -field WICGifImageDescriptorHeight

[VT_UI2] Indicates height of this frame, in pixels.


### -field WICGifImageDescriptorLocalColorTableFlag

[VT_BOOL] Indicates the local color table flag. <b>TRUE</b> if global color table is present; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorInterlaceFlag

[VT_BOOL] Indicates the interlace flag. <b>TRUE</b> if image is interlaced; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorSortFlag

[VT_BOOL] Indicates the sorted color table flag. <b>TRUE</b> if the color table is sorted from most frequently to least frequently used color; otherwise, <b>FALSE</b>.


### -field WICGifImageDescriptorLocalColorTableSize

[VT_UI1] Indicates the value used to calculate the number of bytes contained in the global color table. 

To calculate the actual size of the color table, raise 2 to the value of the field + 1.


### -field WICGifImageDescriptorProperties_FORCE_DWORD



