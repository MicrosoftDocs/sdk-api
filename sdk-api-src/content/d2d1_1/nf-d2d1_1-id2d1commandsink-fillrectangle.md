---
UID: NF:d2d1_1.ID2D1CommandSink.FillRectangle
title: ID2D1CommandSink::FillRectangle (d2d1_1.h)
description: Indicates to the command sink a rectangle to be filled.
helpviewer_keywords: ["FillRectangle","FillRectangle method [Direct2D]","FillRectangle method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","FillRectangle method","ID2D1CommandSink.FillRectangle","ID2D1CommandSink::FillRectangle","d2d1_1/ID2D1CommandSink::FillRectangle","direct2d.id2d1commandsink_fillrectangle"]
old-location: direct2d\id2d1commandsink_fillrectangle.htm
tech.root: Direct2D
ms.assetid: c970a962-8d03-4de8-9252-9babfa411e5f
ms.date: 12/05/2018
ms.keywords: FillRectangle, FillRectangle method [Direct2D], FillRectangle method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillRectangle method, ID2D1CommandSink.FillRectangle, ID2D1CommandSink::FillRectangle, d2d1_1/ID2D1CommandSink::FillRectangle, direct2d.id2d1commandsink_fillrectangle
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
 - ID2D1CommandSink::FillRectangle
 - d2d1_1/ID2D1CommandSink::FillRectangle
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
 - ID2D1CommandSink.FillRectangle
---

# ID2D1CommandSink::FillRectangle


## -description

Indicates to the command sink a rectangle to be filled.

## -parameters

### -param rect [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rectangle to fill.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush with which to fill the rectangle.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)">ID2D1RenderTarget::FillRectangle</a>