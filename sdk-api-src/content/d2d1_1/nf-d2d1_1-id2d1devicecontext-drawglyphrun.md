---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawGlyphRun
title: ID2D1DeviceContext::DrawGlyphRun (d2d1_1.h)
description: Draws a series of glyphs to the device context.
helpviewer_keywords: ["DrawGlyphRun","DrawGlyphRun method [Direct2D]","DrawGlyphRun method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","DrawGlyphRun method","ID2D1DeviceContext.DrawGlyphRun","ID2D1DeviceContext::DrawGlyphRun","d2d1_1/ID2D1DeviceContext::DrawGlyphRun","direct2d.id2d1devicecontext_drawglyphrun"]
old-location: direct2d\id2d1devicecontext_drawglyphrun.htm
tech.root: Direct2D
ms.assetid: a169604c-64d6-401f-83f5-fb322230e110
ms.date: 12/05/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawGlyphRun method, ID2D1DeviceContext.DrawGlyphRun, ID2D1DeviceContext::DrawGlyphRun, d2d1_1/ID2D1DeviceContext::DrawGlyphRun, direct2d.id2d1devicecontext_drawglyphrun
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
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::DrawGlyphRun
 - d2d1_1/ID2D1DeviceContext::DrawGlyphRun
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.DrawGlyphRun
---

# ID2D1DeviceContext::DrawGlyphRun


## -description

Draws a series of glyphs to the device context.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

Origin of first glyph in the series.

### -param glyphRun [in]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.

### -param glyphRunDescription [in, optional]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run_description">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Supplementary glyph series information.

### -param foregroundBrush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush that defines the text color.

### -param measuringMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring mode of the glyph series, used to determine the advances and offsets. The default value is DWRITE_MEASURING_MODE_NATURAL.

## -remarks

The <i>glyphRunDescription</i> is ignored when rendering, but can be useful for printing and serialization of rendering commands, such as to an XPS or SVG file. This extends <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun">ID2D1RenderTarget::DrawGlyphRun</a>, which lacked the glyph run description.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun">ID2D1RenderTarget::DrawGlyphRun</a>