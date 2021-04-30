---
UID: NF:d2d1.ID2D1RenderTarget.DrawTextLayout
title: ID2D1RenderTarget::DrawTextLayout (d2d1.h)
description: Draws the formatted text described by the specified IDWriteTextLayout object.
helpviewer_keywords: ["DrawTextLayout","DrawTextLayout method [Direct2D]","DrawTextLayout method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawTextLayout method","ID2D1RenderTarget.DrawTextLayout","ID2D1RenderTarget::DrawTextLayout","d2d1/ID2D1RenderTarget::DrawTextLayout","direct2d.ID2D1RenderTarget_DrawTextLayout"]
old-location: direct2d\ID2D1RenderTarget_DrawTextLayout.htm
tech.root: Direct2D
ms.assetid: 9356071a-35ca-462a-8a77-887e63850586
ms.date: 12/05/2018
ms.keywords: DrawTextLayout, DrawTextLayout method [Direct2D], DrawTextLayout method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawTextLayout method, ID2D1RenderTarget.DrawTextLayout, ID2D1RenderTarget::DrawTextLayout, d2d1/ID2D1RenderTarget::DrawTextLayout, direct2d.ID2D1RenderTarget_DrawTextLayout
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
 - ID2D1RenderTarget::DrawTextLayout
 - d2d1/ID2D1RenderTarget::DrawTextLayout
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
 - ID2D1RenderTarget.DrawTextLayout
---

# ID2D1RenderTarget::DrawTextLayout


## -description

Draws the formatted text described by the specified <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object.

## -parameters

### -param origin

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point, described in device-independent pixels, at which the upper-left corner of the text described by <i>textLayout</i> is drawn.

### -param textLayout [in]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>*</b>

The formatted text to draw. Any drawing effects that do not inherit from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a> are ignored. If there are drawing effects that inherit from <b>ID2D1Resource</b> that are not brushes, this method fails and the render target is put in an error state.

### -param defaultFillBrush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint any text in <i>textLayout</i> that does not already have a brush associated with it as a drawing effect (specified by the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect">IDWriteTextLayout::SetDrawingEffect</a> method).

### -param options

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS</a></b>

A value that indicates whether the text should be snapped to pixel boundaries and whether the text should be clipped to the layout rectangle. The default value is <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options">D2D1_DRAW_TEXT_OPTIONS_NONE</a>, which indicates that text should be snapped to pixel boundaries and it should not be clipped to the layout rectangle.

## -remarks

When drawing the same text repeatedly, using the <b>DrawTextLayout</b> method is more efficient than using the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)">DrawText</a> method because the text doesn't need to be formatted and the layout processed with each call.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawTextLayout</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/DirectWrite/text-formatting-and-layout">Text Formatting and Layout</a>

