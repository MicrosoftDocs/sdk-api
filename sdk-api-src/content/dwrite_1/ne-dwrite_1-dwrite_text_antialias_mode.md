---
UID: NE:dwrite_1.DWRITE_TEXT_ANTIALIAS_MODE
title: DWRITE_TEXT_ANTIALIAS_MODE (dwrite_1.h)
author: windows-sdk-content
description: The DWRITE_TEXT_ANTIALIAS_MODE enumeration contains values that specify the type of antialiasing to use for text when the rendering mode calls for antialiasing.
old-location: directwrite\dwrite_text_antialias_mode.htm
tech.root: DirectWrite
ms.assetid: 212B02C9-1265-4870-A059-F292640ECE15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXT_ANTIALIAS_MODE, DWRITE_TEXT_ANTIALIAS_MODE enumeration [Direct Write], DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE, DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE, directwrite.dwrite_text_antialias_mode, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE
ms.topic: enum
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_TEXT_ANTIALIAS_MODE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

