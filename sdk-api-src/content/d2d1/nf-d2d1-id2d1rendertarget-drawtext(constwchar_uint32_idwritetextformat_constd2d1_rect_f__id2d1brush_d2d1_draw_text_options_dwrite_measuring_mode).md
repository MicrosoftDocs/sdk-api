---
UID: NF:d2d1.ID2D1RenderTarget.DrawText(constWCHAR,UINT32,IDWriteTextFormat,constD2D1_RECT_F&,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)
title: ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE) (d2d1.h)
description: Draws the specified text using the format information provided by an IDWriteTextFormat object. (overload 1/2)
helpviewer_keywords: ["DrawText","DrawText method [Direct2D]","DrawText method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawText method","ID2D1RenderTarget.DrawText","ID2D1RenderTarget.DrawText(const WCHAR","UINT32","IDWriteTextFormat","const D2D1_RECT_F &","ID2D1Brush","D2D1_DRAW_TEXT_OPTIONS","DWRITE_MEASURING_MODE)","ID2D1RenderTarget::DrawText","ID2D1RenderTarget::DrawText(const WCHAR","UINT32","IDWriteTextFormat","const D2D1_RECT_F &","ID2D1Brush","D2D1_DRAW_TEXT_OPTIONS","DWRITE_MEASURING_MODE)","d2d1/ID2D1RenderTarget::DrawText","direct2d.ID2D1RenderTarget_DrawText_ptr_WCHAR_ptr_IDWriteTextFormat_ref_D2D_RECT_F_ptr_ID2D1Brush_D2D1_DRAW_TEXT_OPTIONS_DWRITE_TEXT_MEASURING_METHOD"]
old-location: direct2d\ID2D1RenderTarget_DrawText_ptr_WCHAR_ptr_IDWriteTextFormat_ref_D2D_RECT_F_ptr_ID2D1Brush_D2D1_DRAW_TEXT_OPTIONS_DWRITE_TEXT_MEASURING_METHOD.htm
tech.root: Direct2D
ms.assetid: 226de985-0d7a-4891-83a0-b1f022ff8bd3
ms.date: 12/05/2018
ms.keywords: DrawText, DrawText method [Direct2D], DrawText method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawText method, ID2D1RenderTarget.DrawText, ID2D1RenderTarget.DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), ID2D1RenderTarget::DrawText, ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE), d2d1/ID2D1RenderTarget::DrawText, direct2d.ID2D1RenderTarget_DrawText_ptr_WCHAR_ptr_IDWriteTextFormat_ref_D2D_RECT_F_ptr_ID2D1Brush_D2D1_DRAW_TEXT_OPTIONS_DWRITE_TEXT_MEASURING_METHOD
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
 - ID2D1RenderTarget::DrawText
 - d2d1/ID2D1RenderTarget::DrawText
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
 - ID2D1RenderTarget.DrawText
---

# ID2D1RenderTarget::DrawText(const WCHAR,UINT32,IDWriteTextFormat,const D2D1_RECT_F &,ID2D1Brush,D2D1_DRAW_TEXT_OPTIONS,DWRITE_MEASURING_MODE)


## -description

Draws the specified text using the format information provided by an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a> object.

## -parameters

### -param string [in]

Type: <b>WCHAR*</b>

A pointer to an array of Unicode characters to draw.

### -param stringLength

Type: <b>UINT</b>

The number of characters in <i>string</i>.

### -param textFormat [in]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>*</b>

An object that describes formatting details of the text to draw, such as the font, the font size, and flow direction.

### -param layoutRect [ref]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The size and position of the area in which the text is drawn.

### -param defaultFillBrush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the text.

### -param options

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. The default value is <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

A value that indicates how glyph metrics are used to measure text when it is formatted.  The default value is <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE_NATURAL</a>.

## -remarks

To create an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a> object, create an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a> and call its <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat">CreateTextFormat</a> method.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/Direct2D/id2d1rendertarget-drawtext">DrawText</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


## Examples

For an example, see <a href="/windows/win32/Direct2D/how-to--draw-text">How to: Draw Text</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">DrawTextLayout</a>



<a href="/windows/win32/Direct2D/how-to--draw-text">How to: Draw Text</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/DirectWrite/text-formatting-and-layout">Text Formatting and Layout</a>

