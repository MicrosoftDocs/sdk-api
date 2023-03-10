---
UID: NF:dwrite.IDWriteTextRenderer.DrawGlyphRun
title: IDWriteTextRenderer::DrawGlyphRun (dwrite.h)
description: IDWriteTextLayout::Draw calls this function to instruct the client to render a run of glyphs. (IDWriteTextRenderer.DrawGlyphRun)
helpviewer_keywords: ["DrawGlyphRun","DrawGlyphRun method [Direct Write]","DrawGlyphRun method [Direct Write]","IDWriteTextRenderer interface","IDWriteTextRenderer interface [Direct Write]","DrawGlyphRun method","IDWriteTextRenderer.DrawGlyphRun","IDWriteTextRenderer::DrawGlyphRun","directwrite.IDWriteTextRenderer_DrawGlyphRun","dwrite/IDWriteTextRenderer::DrawGlyphRun"]
old-location: directwrite\IDWriteTextRenderer_DrawGlyphRun.htm
tech.root: DirectWrite
ms.assetid: 95a0044c-dffd-4c6a-a6eb-2f87b02ef89a
ms.date: 12/05/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct Write], DrawGlyphRun method [Direct Write],IDWriteTextRenderer interface, IDWriteTextRenderer interface [Direct Write],DrawGlyphRun method, IDWriteTextRenderer.DrawGlyphRun, IDWriteTextRenderer::DrawGlyphRun, directwrite.IDWriteTextRenderer_DrawGlyphRun, dwrite/IDWriteTextRenderer::DrawGlyphRun
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
 - IDWriteTextRenderer::DrawGlyphRun
 - dwrite/IDWriteTextRenderer::DrawGlyphRun
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
 - IDWriteTextRenderer.DrawGlyphRun
---

# IDWriteTextRenderer::DrawGlyphRun


## -description

 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to
     render a run of glyphs.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a>.

### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the glyph run.

### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the glyph run.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

Pointer to the glyph run instance to render.

### -param glyphRunDescription [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description">DWRITE_GLYPH_RUN_DESCRIPTION</a>*</b>

A pointer to the glyph run description instance which contains properties of the characters 
     associated with this run.

### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects for the glyphs to render. Usually this argument represents effects such as the foreground brush filling the interior of text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> function calls this callback function with all the information about glyphs to render. The application implements this callback by mostly delegating the call to the underlying platform's graphics API such as <a href="/windows/win32/Direct2D/direct2d-portal">Direct2D</a> to draw glyphs on the drawing context. An application that uses GDI can implement this callback in terms of the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun">IDWriteBitmapRenderTarget::DrawGlyphRun</a> method.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a>

