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

# WMT_IMAGE_TYPE enumeration


## -description



The <b>WMT_IMAGE_TYPE</b> enumeration type defines the types of images that can be used for banner ads. This type is used as the value of the <a href="https://msdn.microsoft.com/e751cc73-8960-4ec8-9bff-b2cd06df7919">BannerImageType</a> attribute.




## -enum-fields




### -field WMT_IT_NONE

There is no image. If a <a href="https://msdn.microsoft.com/ce9b0692-ae0b-4a23-b38c-3a1df830fac2">BannerImageData</a> attribute in the file, it will be ignored.


### -field WMT_IT_BITMAP

The banner image is an uncompressed bitmap.


### -field WMT_IT_JPEG

The banner image uses JPEG encoding.


### -field WMT_IT_GIF

The banner image uses GIF encoding.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

