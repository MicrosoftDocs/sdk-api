---
UID: NS:d2d1_1.D2D1_BITMAP_PROPERTIES1
title: D2D1_BITMAP_PROPERTIES1
author: windows-sdk-content
description: This structure allows a ID2D1Bitmap1 to be created with bitmap options and color context information available.
old-location: direct2d\d2d1_bitmap_properties1.htm
tech.root: direct2d
ms.assetid: c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_BITMAP_PROPERTIES1, D2D1_BITMAP_PROPERTIES1 structure [Direct2D], PD2D1_BITMAP_PROPERTIES1, PD2D1_BITMAP_PROPERTIES1 structure pointer [Direct2D], d2d1_1/D2D1_BITMAP_PROPERTIES1, d2d1_1/PD2D1_BITMAP_PROPERTIES1, direct2d.d2d1_bitmap_properties1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_BITMAP_PROPERTIES1
product: Windows
targetos: Windows
req.typenames: D2D1_BITMAP_PROPERTIES1
req.redist: 
---

# D2D1_BITMAP_PROPERTIES1 structure


## -description


This structure allows a <a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a> to be created with bitmap options and color context information available.



## -struct-fields




### -field pixelFormat

Type: <b><a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a></b>

The DXGI format and alpha mode to create the bitmap with.


### -field dpiX

Type: <b>FLOAT</b>

The bitmap dpi in the x direction.


### -field dpiY

Type: <b>FLOAT</b>

The bitmap dpi in the y direction.


### -field bitmapOptions

Type: <b><a href="https://msdn.microsoft.com/c080e23e-99c4-46ed-8b21-be26dec288af">D2D1_BITMAP_OPTIONS</a></b>

The special creation options of the bitmap.


### -field colorContext

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>*</b>

The optionally specified color context information.


## -remarks



If both <b>dpiX</b> and <b>dpiY</b> are 0, the dpi of the bitmap will be set to the desktop dpi if the device context is a windowed context, or 96 dpi for any other device context.




## -see-also




<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>
 

 

