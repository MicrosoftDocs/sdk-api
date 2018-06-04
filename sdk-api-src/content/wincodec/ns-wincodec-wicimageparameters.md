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

# WICImageParameters structure


## -description


This defines parameters that you can use to override the default parameters normally used when encoding an image. 


## -struct-fields




### -field PixelFormat

The pixel format to which the image is processed before it is written to the encoder.


### -field DpiX

The DPI in the x dimension.


### -field DpiY

The DPI in the y dimension.


### -field Top

The top corner in pixels of the image space to be encoded to the destination.


### -field Left

The left corner in pixels of the image space to be encoded to the destination.


### -field PixelWidth

The width in pixels of the part of the image to write.


### -field PixelHeight

The height in pixels of the part of the image to write.


## -remarks



If this parameter is not passed to the encoding API, the encoder uses these settings.

<ul>
<li>A pixel format of (<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM</a>, <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_PREMULTIPLIED</a>).</li>
<li>An x and y DPI of 96.</li>
<li>The entire image bounds will be used for encoding.</li>
</ul>
<div class="alert"><b>Note</b>  The parameters as specified can't result in a scale. The encoder can use a larger portion of the input image based on the passed in DPI and the pixel width and height.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a>
 

 

