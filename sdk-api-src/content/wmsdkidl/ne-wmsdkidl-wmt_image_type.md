---
UID: NE:wmsdkidl.WMT_IMAGE_TYPE
title: WMT_IMAGE_TYPE
author: windows-sdk-content
description: The WMT_IMAGE_TYPE enumeration type defines the types of images that can be used for banner ads. This type is used as the value of the BannerImageType attribute.
old-location: wmformat\wmt_image_type.htm
old-project: wmformat
ms.assetid: 727cfed7-d818-4c0f-9e9f-a35d9a8c195e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: WMT_IMAGE_TYPE, WMT_IMAGE_TYPE enumeration [windows Media Format], WMT_IT_BITMAP, WMT_IT_GIF, WMT_IT_JPEG, WMT_IT_NONE, wmformat.wmt_image_type, wmsdkidl/WMT_IMAGE_TYPE, wmsdkidl/WMT_IT_BITMAP, wmsdkidl/WMT_IT_GIF, wmsdkidl/WMT_IT_JPEG, wmsdkidl/WMT_IT_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMT_IMAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_IMAGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

