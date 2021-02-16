---
UID: NF:d2d1_1.ID2D1CommandSink.DrawRectangle
title: ID2D1CommandSink::DrawRectangle (d2d1_1.h)
description: Draws a rectangle.
helpviewer_keywords: ["DrawRectangle","DrawRectangle method [Direct2D]","DrawRectangle method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawRectangle method","ID2D1CommandSink.DrawRectangle","ID2D1CommandSink::DrawRectangle","d2d1_1/ID2D1CommandSink::DrawRectangle","direct2d.id2d1commandsink_drawrectangle"]
old-location: direct2d\id2d1commandsink_drawrectangle.htm
tech.root: Direct2D
ms.assetid: 93c617fb-3c9d-4735-a077-7a3a58033369
ms.date: 12/05/2018
ms.keywords: DrawRectangle, DrawRectangle method [Direct2D], DrawRectangle method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawRectangle method, ID2D1CommandSink.DrawRectangle, ID2D1CommandSink::DrawRectangle, d2d1_1/ID2D1CommandSink::DrawRectangle, direct2d.id2d1commandsink_drawrectangle
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
 - ID2D1CommandSink::DrawRectangle
 - d2d1_1/ID2D1CommandSink::DrawRectangle
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
 - ID2D1CommandSink.DrawRectangle
---

# ID2D1CommandSink::DrawRectangle


## -description

Draws a rectangle.

## -parameters

### -param rect [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rectangle to be drawn to the command sink.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to stroke the geometry.

### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of the stroke.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)">ID2D1RenderTarget::DrawRectangle</a>