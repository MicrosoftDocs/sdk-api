---
UID: NF:d2d1_1.ID2D1CommandSink.DrawGlyphRun
title: ID2D1CommandSink::DrawGlyphRun (d2d1_1.h)
description: Indicates the glyphs to be drawn.
helpviewer_keywords: ["DrawGlyphRun","DrawGlyphRun method [Direct2D]","DrawGlyphRun method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawGlyphRun method","ID2D1CommandSink.DrawGlyphRun","ID2D1CommandSink::DrawGlyphRun","d2d1_1/ID2D1CommandSink::DrawGlyphRun","direct2d.id2d1commandsink_drawglyphrun"]
old-location: direct2d\id2d1commandsink_drawglyphrun.htm
tech.root: Direct2D
ms.assetid: 5b40a999-0046-458e-b7bc-95037d73833c
ms.date: 12/05/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct2D], DrawGlyphRun method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawGlyphRun method, ID2D1CommandSink.DrawGlyphRun, ID2D1CommandSink::DrawGlyphRun, d2d1_1/ID2D1CommandSink::DrawGlyphRun, direct2d.id2d1commandsink_drawglyphrun
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
 - ID2D1CommandSink::DrawGlyphRun
 - d2d1_1/ID2D1CommandSink::DrawGlyphRun
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
 - ID2D1CommandSink.DrawGlyphRun
---

# ID2D1CommandSink::DrawGlyphRun


## -description

Indicates the glyphs to be drawn.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The upper left corner of the baseline.

### -param glyphRun [in]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyphs to render.

### -param glyphRunDescription [in, optional]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run_description">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

Additional non-rendering information about the glyphs.

### -param foregroundBrush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to fill the glyphs.

### -param measuringMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring mode to apply to the glyphs.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/Direct2D/id2d1rendertarget-drawtext">DrawText</a> and <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">DrawTextLayout</a> are broken down into glyph runs and rectangles by the time the command sink is processed. So, these methods aren't available on the command sink. Since the application may require additional callback processing when calling <b>DrawTextLayout</b>, this semantic can't be easily preserved in the command list.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun">ID2D1DeviceContext::DrawGlyphRun</a>