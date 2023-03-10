---
UID: NF:dwrite.IDWriteTextLayout.SetDrawingEffect
title: IDWriteTextLayout::SetDrawingEffect (dwrite.h)
description: Sets the application-defined drawing effect.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetDrawingEffect method","IDWriteTextLayout.SetDrawingEffect","IDWriteTextLayout::SetDrawingEffect","SetDrawingEffect","SetDrawingEffect method [Direct Write]","SetDrawingEffect method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetDrawingEffect","dwrite/IDWriteTextLayout::SetDrawingEffect"]
old-location: directwrite\IDWriteTextLayout_SetDrawingEffect.htm
tech.root: DirectWrite
ms.assetid: d3269f8e-c1bc-4e84-92cb-a8899a0268ff
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetDrawingEffect method, IDWriteTextLayout.SetDrawingEffect, IDWriteTextLayout::SetDrawingEffect, SetDrawingEffect, SetDrawingEffect method [Direct Write], SetDrawingEffect method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetDrawingEffect, dwrite/IDWriteTextLayout::SetDrawingEffect
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
 - IDWriteTextLayout::SetDrawingEffect
 - dwrite/IDWriteTextLayout::SetDrawingEffect
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
 - IDWriteTextLayout.SetDrawingEffect
---

# IDWriteTextLayout::SetDrawingEffect


## -description

 Sets the application-defined drawing effect.

## -parameters

### -param drawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects that apply to the range. This data object will be passed back to the application's drawing callbacks for final rendering.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

The text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>, such as a color or gradient brush, can be set as a drawing effect if you are using the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">ID2D1RenderTarget::DrawTextLayout</a> to draw text and that brush will be used to draw the specified range of text.

 This drawing effect is associated with the specified range and will be passed back
     to the application by way of the callback when the range is drawn at drawing time.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

