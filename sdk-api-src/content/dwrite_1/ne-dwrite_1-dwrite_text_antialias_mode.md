---
UID: NE:dwrite_1.DWRITE_TEXT_ANTIALIAS_MODE
title: DWRITE_TEXT_ANTIALIAS_MODE (dwrite_1.h)
description: The DWRITE_TEXT_ANTIALIAS_MODE enumeration contains values that specify the type of antialiasing to use for text when the rendering mode calls for antialiasing.
helpviewer_keywords: ["DWRITE_TEXT_ANTIALIAS_MODE","DWRITE_TEXT_ANTIALIAS_MODE enumeration [Direct Write]","DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE","DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE","directwrite.dwrite_text_antialias_mode","dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE","dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE","dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE"]
old-location: directwrite\dwrite_text_antialias_mode.htm
tech.root: DirectWrite
ms.assetid: 212B02C9-1265-4870-A059-F292640ECE15
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXT_ANTIALIAS_MODE, DWRITE_TEXT_ANTIALIAS_MODE enumeration [Direct Write], DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE, DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE, directwrite.dwrite_text_antialias_mode, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE, dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_TEXT_ANTIALIAS_MODE
 - dwrite_1/DWRITE_TEXT_ANTIALIAS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_TEXT_ANTIALIAS_MODE
---

# DWRITE_TEXT_ANTIALIAS_MODE enumeration


## -description

The <b>DWRITE_TEXT_ANTIALIAS_MODE</b> enumeration contains values that specify the type of antialiasing to use for text when the rendering mode calls for antialiasing.

## -enum-fields

### -field DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE

ClearType antialiasing computes coverage independently for the red, green, and blue color elements of each pixel. This allows for more detail than conventional antialiasing. However, because there is no one alpha value for each pixel, ClearType is not suitable for rendering text onto a transparent intermediate bitmap.

### -field DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE

Grayscale antialiasing computes one coverage value for each pixel. Because the alpha value of each pixel is well-defined, text can be rendered onto a transparent bitmap, which can then be composited with other content.

<div class="alert"><b>Note</b>  Grayscale rendering with <a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1">IDWriteBitmapRenderTarget1</a> uses premultiplied alpha.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritebitmaprendertarget1-gettextantialiasmode">IDWriteBitmapRenderTarget1::GetTextAntialiasMode</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritebitmaprendertarget1-settextantialiasmode">IDWriteBitmapRenderTarget1::SetTextAntialiasMode</a>

