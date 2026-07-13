---
UID: NF:dwrite_3.IDWriteFontFace3.GetRecommendedRenderingMode
title: IDWriteFontFace3::GetRecommendedRenderingMode (dwrite_3.h)
description: Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode. (IDWriteFontFace3.GetRecommendedRenderingMode)
helpviewer_keywords: ["GetRecommendedRenderingMode","GetRecommendedRenderingMode method [Direct Write]","GetRecommendedRenderingMode method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","GetRecommendedRenderingMode method","IDWriteFontFace3.GetRecommendedRenderingMode","IDWriteFontFace3::GetRecommendedRenderingMode","directwrite.idwritefontface3_getrecommendedrenderingmode","dwrite_3/IDWriteFontFace3::GetRecommendedRenderingMode"]
old-location: directwrite\idwritefontface3_getrecommendedrenderingmode.htm
tech.root: DirectWrite
ms.assetid: 9EF4A414-8DD9-431B-81A6-D87F4CF9AA73
ms.date: 09/10/2025
ms.keywords: GetRecommendedRenderingMode, GetRecommendedRenderingMode method [Direct Write], GetRecommendedRenderingMode method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetRecommendedRenderingMode method, IDWriteFontFace3.GetRecommendedRenderingMode, IDWriteFontFace3::GetRecommendedRenderingMode, directwrite.idwritefontface3_getrecommendedrenderingmode, dwrite_3/IDWriteFontFace3::GetRecommendedRenderingMode
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3::GetRecommendedRenderingMode
 - dwrite_3/IDWriteFontFace3::GetRecommendedRenderingMode
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
 - IDWriteFontFace3.GetRecommendedRenderingMode
---

# IDWriteFontFace3::GetRecommendedRenderingMode


## -description

Determines the recommended text rendering and grid-fit mode to be used based on the font, size, world transform, and measuring mode.

## -parameters

### -param fontEmSize [in]

Type: <b>FLOAT</b>

Logical font size in DIPs.

### -param dpiX [in]

Type: <b>FLOAT</b>

Number of pixels per logical inch in the horizontal direction.

### -param dpiY [in]

Type: <b>FLOAT</b>

Number of pixels per logical inch in the vertical direction.

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

A <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a> structure that describes the world transform.

### -param isSideways [in]

Type: <b>BOOL</b>

Specifies whether the font is sideways. <b>TRUE</b> if the font is sideways; otherwise, <b>FALSE</b>.

### -param outlineThreshold [in]

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_outline_threshold">DWRITE_OUTLINE_THRESHOLD</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_outline_threshold">DWRITE_OUTLINE_THRESHOLD</a>-typed value that specifies the quality of the graphics system's outline rendering, affects the size threshold above which outline rendering is used.

### -param measuringMode [in]

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

A <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a>-typed value that specifies  the method used to measure during text layout. For proper glyph spacing, this method returns a rendering mode that is compatible with the specified measuring mode.

### -param renderingParams [in, optional]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a> interface for the rendering parameters object. This parameter is necessary in case the rendering parameters object overrides the rendering mode.

### -param renderingMode [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1">DWRITE_RENDERING_MODE1</a>*</b>

A pointer to a variable that receives a <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1">DWRITE_RENDERING_MODE1</a>-typed value for the recommended rendering mode.

### -param gridFitMode [out]

Type: <b><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode">DWRITE_GRID_FIT_MODE</a>*</b>

A pointer to a variable that receives a <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode">DWRITE_GRID_FIT_MODE</a>-typed value for the recommended grid-fit mode.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

