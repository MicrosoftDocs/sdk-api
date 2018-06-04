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

# WICBitmapPlane structure


## -description


Specifies the pixel format, buffer, stride and size of a component plane for a planar pixel format.


## -struct-fields




### -field Format

Type: <b>WICPixelFormatGUID</b>

Describes the pixel format of the plane. 


### -field pbBuffer

Type: <b>BYTE*</b>

Pointer to the buffer that holds the plane’s pixel components.


### -field cbStride

Type: <b>UINT</b>

The stride of the buffer ponted to by <i>pbData</i>.  Stride indicates the total number of bytes to go from the beginning of one scanline to the beginning of the next scanline.


### -field cbBufferSize

Type: <b>UINT</b>

The total size of the buffer pointed to by <i>pbBuffer</i>.


## -see-also




<a href="https://msdn.microsoft.com/0D6FB12B-B5C5-4A36-93FC-AF96BF03ED01">IWICPlanarBitmapSourceTransform::CopyPixels</a>



<a href="https://msdn.microsoft.com/CB601454-591B-4292-A8BF-EA9D1F060AB3">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>
 

 

