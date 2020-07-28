---
UID: NF:d2d1_3.ID2D1DeviceContext4.DrawText(constWCHAR,UINT32,IDWriteTextFormat,constD2D1_RECT_F,ID2D1Brush,ID2D1SvgGlyphStyle,UINT32,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)
title: ID2D1DeviceContext4::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F,ID2D1Brush,ID2D1SvgGlyphStyle,UINT32,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE) (d2d1_3.h)
description: Draws the text within the given layout rectangle.
helpviewer_keywords: ["DrawText","DrawText method [Direct2D]","DrawText method [Direct2D]","ID2D1DeviceContext4 interface","ID2D1DeviceContext4 interface [Direct2D]","DrawText method","ID2D1DeviceContext4.DrawText","ID2D1DeviceContext4.DrawText(const WCHAR","UINT32","IDWriteTextFormat","const D2D1_RECT_F","ID2D1Brush","ID2D1SvgGlyphStyle","UINT32","D2D1_DRAW_TEXT_OPTIONS","DWRITE_MEASURING_MODE)","ID2D1DeviceContext4::DrawText","ID2D1DeviceContext4::DrawText(const WCHAR","UINT32","IDWriteTextFormat","const D2D1_RECT_F","ID2D1Brush","ID2D1SvgGlyphStyle","UINT32","D2D1_DRAW_TEXT_OPTIONS","DWRITE_MEASURING_MODE)","d2d1_3/ID2D1DeviceContext4::DrawText","direct2d.id2d1devicecontext4_drawtext"]
old-location: direct2d\id2d1devicecontext4_drawtext.htm
tech.root: Direct2D
ms.assetid: 7C701D94-5DBB-4143-B88B-A0D7BB124FC5
ms.date: 12/05/2018
ms.keywords: DrawText, DrawText method [Direct2D], DrawText method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],DrawText method, ID2D1DeviceContext4.DrawText, ID2D1DeviceContext4.DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F,ID2D1Brush,ID2D1SvgGlyphStyle,UINT32,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), ID2D1DeviceContext4::DrawText, ID2D1DeviceContext4::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F,ID2D1Brush,ID2D1SvgGlyphStyle,UINT32,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), d2d1_3/ID2D1DeviceContext4::DrawText, direct2d.id2d1devicecontext4_drawtext
f1_keywords:
- d2d1_3/ID2D1DeviceContext4.DrawText
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1DeviceContext4.DrawText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext4::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F,ID2D1Brush,ID2D1SvgGlyphStyle,UINT32,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)


## -description


Draws the text within the given layout rectangle.

By default, this method performs baseline snapping and renders color versions of glyphs in color fonts.


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

A pointer to an array of Unicode characters to draw.


### -param stringLength

Type: <b>UINT32</b>

The number of characters in string.


### -param textFormat [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>*</b>

An object that describes formatting details of the text to draw, such as the font, the font size, and flow direction.


### -param layoutRect [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The size and position of the area in which the text is drawn.


### -param defaultFillBrush [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the text.


### -param svgGlyphStyle [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1svgglyphstyle">ID2D1SvgGlyphStyle</a>*</b>

Values for context-fill, context-stroke, and context-value that are used when rendering SVG glyphs.


### -param colorPaletteIndex

Type: <b>UINT32</b>

The index used to select a color palette within a color font.


### -param options

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. 
          The default value is <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, 
          which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.


### -param measuringMode

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

A value that indicates how glyph metrics are used to measure text when it is formatted. 
          The default value is <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>
 

 

