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

# WICGifLogicalScreenDescriptorProperties enumeration


## -description


Specifies the logical screen descriptor properties for Graphics Interchange Format (GIF) metadata.


## -enum-fields




### -field WICGifLogicalScreenSignature

 [VT_UI1 | VT_VECTOR] Indicates the signature property.


### -field WICGifLogicalScreenDescriptorWidth

[VT_UI2] Indicates the width in pixels. 


### -field WICGifLogicalScreenDescriptorHeight

[VT_UI2] Indicates the height in pixels. 


### -field WICGifLogicalScreenDescriptorGlobalColorTableFlag

[VT_BOOL] Indicates the  global color table flag. <b>TRUE</b> if a global color table is present; otherwise, <b>FALSE</b>.


### -field WICGifLogicalScreenDescriptorColorResolution

[VT_UI1] Indicates the color resolution in bits per pixel.


### -field WICGifLogicalScreenDescriptorSortFlag

[VT_BOOL] Indicates the sorted color table flag. <b>TRUE</b> if the table is sorted; otherwise, <b>FALSE</b>.


### -field WICGifLogicalScreenDescriptorGlobalColorTableSize

[VT_UI1] Indicates the value used to calculate the number of bytes contained in the global color table. 

To calculate the actual size of the color table, raise 2 to the value of the field + 1.


### -field WICGifLogicalScreenDescriptorBackgroundColorIndex

[VT_UI1] Indicates the index within the color table to use for the background (pixels not defined in the image).


### -field WICGifLogicalScreenDescriptorPixelAspectRatio

[VT_UI1] Indicates the factor used to compute an approximation of the aspect ratio.


### -field WICGifLogicalScreenDescriptorProperties_FORCE_DWORD



