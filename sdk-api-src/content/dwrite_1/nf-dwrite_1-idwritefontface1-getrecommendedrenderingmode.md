---
UID: NF:dwrite_1.IDWriteFontFace1.GetRecommendedRenderingMode
title: IDWriteFontFace1::GetRecommendedRenderingMode (dwrite_1.h)
description: Determines the recommended rendering mode for the font, using the specified size and rendering parameters. (IDWriteFontFace1.GetRecommendedRenderingMode)
helpviewer_keywords: ["GetRecommendedRenderingMode","GetRecommendedRenderingMode method [Direct Write]","GetRecommendedRenderingMode method [Direct Write]","IDWriteFontFace1 interface","IDWriteFontFace1 interface [Direct Write]","GetRecommendedRenderingMode method","IDWriteFontFace1.GetRecommendedRenderingMode","IDWriteFontFace1::GetRecommendedRenderingMode","directwrite.idwritefontface1_getrecommendedrenderingmode","dwrite_1/IDWriteFontFace1::GetRecommendedRenderingMode"]
old-location: directwrite\idwritefontface1_getrecommendedrenderingmode.htm
tech.root: DirectWrite
ms.assetid: 4726A5FC-6481-4986-AE2D-EBC044D0B9C6
ms.date: 12/05/2018
ms.keywords: GetRecommendedRenderingMode, GetRecommendedRenderingMode method [Direct Write], GetRecommendedRenderingMode method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetRecommendedRenderingMode method, IDWriteFontFace1.GetRecommendedRenderingMode, IDWriteFontFace1::GetRecommendedRenderingMode, directwrite.idwritefontface1_getrecommendedrenderingmode, dwrite_1/IDWriteFontFace1::GetRecommendedRenderingMode
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace1::GetRecommendedRenderingMode
 - dwrite_1/IDWriteFontFace1::GetRecommendedRenderingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetRecommendedRenderingMode
---

# IDWriteFontFace1::GetRecommendedRenderingMode


## -description

 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

## -parameters

### -param fontEmSize

Type: <b>FLOAT</b>

The logical size of the font in DIP units. A DIP ("device-independent pixel") equals 1/96 inch.

### -param dpiX

Type: <b>FLOAT</b>

The number of physical pixels per DIP in a horizontal position. For example, if the DPI of the rendering surface is 96, this 
     value is 1.0f. If the DPI is 120, this value is 120.0f/96.

### -param dpiY

Type: <b>FLOAT</b>

The number of physical pixels per DIP in a vertical position. For example, if the DPI of the rendering surface is 96, this 
     value is 1.0f. If the DPI is 120, this value is 120.0f/96.

### -param transform [in, optional]

Type: <b>const DWRITE_MATRIX*</b>

Specifies the world transform.

### -param isSideways

Type: <b>BOOL</b>

Whether the glyphs in the run are sideways or not.

### -param outlineThreshold

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_outline_threshold">DWRITE_OUTLINE_THRESHOLD</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_outline_threshold">DWRITE_OUTLINE_THRESHOLD</a>-typed value that specifies the quality of the graphics system's outline rendering,
    affects the size threshold above which outline rendering is used.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring method that will be used for glyphs in the font.
     Renderer implementations may choose different rendering modes for different measuring methods, for example:
     

<ul>
<li>DWRITE_RENDERING_MODE_CLEARTYPE_NATURAL for <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>
</li>
<li>DWRITE_RENDERING_MODE_CLEARTYPE_GDI_CLASSIC for <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_GDI_CLASSIC</a>
</li>
<li>DWRITE_RENDERING_MODE_CLEARTYPE_GDI_NATURAL for <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_GDI_NATURAL</a>
</li>
</ul>

### -param renderingMode [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a>*</b>

When this method returns, contains a value that indicates the recommended rendering mode to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be used to determine the actual rendering mode in cases where the rendering 
    mode of the rendering params object is DWRITE_RENDERING_MODE_DEFAULT.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>

