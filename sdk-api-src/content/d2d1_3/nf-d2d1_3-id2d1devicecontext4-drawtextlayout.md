---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawTextLayout
title: ID2D1DeviceContext4::DrawTextLayout (d2d1_3.h)
description: Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.
helpviewer_keywords: ["DrawTextLayout","DrawTextLayout method [Direct2D]","DrawTextLayout method [Direct2D]","ID2D1DeviceContext4 interface","ID2D1DeviceContext4 interface [Direct2D]","DrawTextLayout method","ID2D1DeviceContext4.DrawTextLayout","ID2D1DeviceContext4::DrawTextLayout","d2d1_3/ID2D1DeviceContext4::DrawTextLayout","direct2d.id2d1devicecontext4_drawtextlayout"]
old-location: direct2d\id2d1devicecontext4_drawtextlayout.htm
tech.root: Direct2D
ms.assetid: 54993EFD-A649-4613-8A9C-744FE22F7BFC
ms.date: 12/05/2018
ms.keywords: DrawTextLayout, DrawTextLayout method [Direct2D], DrawTextLayout method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawTextLayout method, ID2D1DeviceContext4.DrawTextLayout, ID2D1DeviceContext4::DrawTextLayout, d2d1_3/ID2D1DeviceContext4::DrawTextLayout, direct2d.id2d1devicecontext4_drawtextlayout
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext4::DrawTextLayout
 - d2d1_3/ID2D1DeviceContext4::DrawTextLayout
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
 - ID2D1DeviceContext4.DrawTextLayout
---

# ID2D1DeviceContext4::DrawTextLayout


## -description

Draws a text layout object. If the layout is not subsequently changed, this can be more efficient than DrawText when drawing the same layout repeatedly.

## -parameters

### -param origin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point, described in device-independent pixels, at which the upper-left corner of the text described by <i>textLayout</i> is drawn.

### -param textLayout [in]

Type: <b><a href="/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>*</b>

The formatted text to draw. Any drawing effects that do not inherit from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a> are ignored. If there are drawing effects that inherit from <b>ID2D1Resource</b> that are not brushes, this method fails and the render target is put in an error state.

### -param defaultFillBrush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the text.

### -param svgGlyphStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>*</b>

The values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.

### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font.

### -param options

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. 
            The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, 
            which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>