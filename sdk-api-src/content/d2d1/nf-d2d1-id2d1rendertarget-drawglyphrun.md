---
UID: NF:d2d1.ID2D1RenderTarget.DrawGlyphRun
title: ID2D1RenderTarget::DrawGlyphRun (d2d1.h)
description: Draws the specified glyphs.
helpviewer_keywords: ["DrawGlyphRun","DrawGlyphRun method [Direct2D]","DrawGlyphRun method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawGlyphRun method","ID2D1RenderTarget.DrawGlyphRun","ID2D1RenderTarget::DrawGlyphRun","d2d1/ID2D1RenderTarget::DrawGlyphRun","direct2d.ID2D1RenderTarget_DrawGlyphRun"]
old-location: direct2d\ID2D1RenderTarget_DrawGlyphRun.htm
tech.root: Direct2D
ms.assetid: 064ede6c-139c-4160-9c50-460179d46f97
ms.date: 12/05/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawGlyphRun method, ID2D1RenderTarget.DrawGlyphRun, ID2D1RenderTarget::DrawGlyphRun, d2d1/ID2D1RenderTarget::DrawGlyphRun, direct2d.ID2D1RenderTarget_DrawGlyphRun
req.header: d2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::DrawGlyphRun
 - d2d1/ID2D1RenderTarget::DrawGlyphRun
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
 - ID2D1RenderTarget.DrawGlyphRun
---

# ID2D1RenderTarget::DrawGlyphRun


## -description

Draws the specified glyphs.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The origin, in device-independent pixels, of the glyphs' baseline.

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.

### -param foregroundBrush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the specified glyphs.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

A value that indicates how glyph metrics are used to measure text when it is formatted.  The default value is <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawGlyphRun</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

