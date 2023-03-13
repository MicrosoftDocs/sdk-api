---
UID: NF:dwrite.IDWriteFontFace.GetRecommendedRenderingMode
title: IDWriteFontFace::GetRecommendedRenderingMode (dwrite.h)
description: Determines the recommended rendering mode for the font, using the specified size and rendering parameters. (IDWriteFontFace.GetRecommendedRenderingMode)
helpviewer_keywords: ["GetRecommendedRenderingMode","GetRecommendedRenderingMode method [Direct Write]","GetRecommendedRenderingMode method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetRecommendedRenderingMode method","IDWriteFontFace.GetRecommendedRenderingMode","IDWriteFontFace::GetRecommendedRenderingMode","directwrite.IDWriteFontFace_GetRecommendedRenderingMode","dwrite/IDWriteFontFace::GetRecommendedRenderingMode"]
old-location: directwrite\IDWriteFontFace_GetRecommendedRenderingMode.htm
tech.root: DirectWrite
ms.assetid: 54504bcb-b05c-4b63-8704-8d718cf2ee16
ms.date: 12/05/2018
ms.keywords: GetRecommendedRenderingMode, GetRecommendedRenderingMode method [Direct Write], GetRecommendedRenderingMode method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetRecommendedRenderingMode method, IDWriteFontFace.GetRecommendedRenderingMode, IDWriteFontFace::GetRecommendedRenderingMode, directwrite.IDWriteFontFace_GetRecommendedRenderingMode, dwrite/IDWriteFontFace::GetRecommendedRenderingMode
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace::GetRecommendedRenderingMode
 - dwrite/IDWriteFontFace::GetRecommendedRenderingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace.GetRecommendedRenderingMode
---

# IDWriteFontFace::GetRecommendedRenderingMode


## -description

 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

## -parameters

### -param emSize

Type: <b>FLOAT</b>

The logical size of the font in DIP units. A DIP ("device-independent pixel") equals 1/96 inch.

### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP. For example, if the DPI of the rendering surface is 96, this 
     value is 1.0f. If the DPI is 120, this value is 120.0f/96.

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

### -param renderingParams

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>*</b>

A pointer to an object that contains rendering settings such as gamma level, enhanced contrast, and ClearType level. This parameter is necessary in case the rendering parameters 
     object overrides the rendering mode.

### -param renderingMode [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a>*</b>

When this method returns, contains a value that indicates the recommended rendering mode to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

