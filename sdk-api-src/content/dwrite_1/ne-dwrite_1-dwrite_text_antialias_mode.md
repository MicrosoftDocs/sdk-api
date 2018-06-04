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

# DWRITE_TEXT_ANTIALIAS_MODE enumeration


## -description


The <b>DWRITE_TEXT_ANTIALIAS_MODE</b> enumeration contains values that specify the type of antialiasing to use for text when the rendering mode calls for antialiasing.


## -enum-fields




### -field DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE

ClearType antialiasing computes coverage independently for the red, green, and blue color elements of each pixel. This allows for more detail than conventional antialiasing. However, because there is no one alpha value for each pixel, ClearType is not suitable for rendering text onto a transparent intermediate bitmap.


### -field DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE

Grayscale antialiasing computes one coverage value for each pixel. Because the alpha value of each pixel is well-defined, text can be rendered onto a transparent bitmap, which can then be composited with other content.

<div class="alert"><b>Note</b>  Grayscale rendering with <a href="https://msdn.microsoft.com/5A7D2723-932B-4707-ABCC-0C0282FB7A56">IDWriteBitmapRenderTarget1</a> uses premultiplied alpha.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/C58E06D8-40CB-488E-BAF3-81A7183564C6">IDWriteBitmapRenderTarget1::GetTextAntialiasMode</a>



<a href="https://msdn.microsoft.com/813C984D-81BC-4CAA-8C0A-166612E8028F">IDWriteBitmapRenderTarget1::SetTextAntialiasMode</a>
 

 

