---
UID: NF:d2d1_1.ID2D1CommandSink.FillOpacityMask
title: ID2D1CommandSink::FillOpacityMask (d2d1_1.h)
description: Fills an opacity mask on the command sink.
helpviewer_keywords: ["FillOpacityMask","FillOpacityMask method [Direct2D]","FillOpacityMask method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","FillOpacityMask method","ID2D1CommandSink.FillOpacityMask","ID2D1CommandSink::FillOpacityMask","d2d1_1/ID2D1CommandSink::FillOpacityMask","direct2d.id2d1commandsink_fillopacitymask"]
old-location: direct2d\id2d1commandsink_fillopacitymask.htm
tech.root: Direct2D
ms.assetid: c125b2db-0786-4bda-b31f-de05ba72afa1
ms.date: 12/05/2018
ms.keywords: FillOpacityMask, FillOpacityMask method [Direct2D], FillOpacityMask method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillOpacityMask method, ID2D1CommandSink.FillOpacityMask, ID2D1CommandSink::FillOpacityMask, d2d1_1/ID2D1CommandSink::FillOpacityMask, direct2d.id2d1commandsink_fillopacitymask
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
 - ID2D1CommandSink::FillOpacityMask
 - d2d1_1/ID2D1CommandSink::FillOpacityMask
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
 - ID2D1CommandSink.FillOpacityMask
---

# ID2D1CommandSink::FillOpacityMask


## -description

Fills an opacity mask on the command sink.

## -parameters

### -param opacityMask [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap whose alpha channel will be sampled to define the opacity mask.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush with which to fill the mask.

### -param destinationRectangle [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The destination rectangle in which to fill the mask. If not specified, this is the origin.

### -param sourceRectangle [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The source rectangle within the opacity mask. If not specified, this is the entire mask.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The opacity mask bitmap must be considered to be clamped on each axis.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/Direct2D/id2d1rendertarget-fillopacitymask">ID2D1RenderTarget::FillOpacityMask</a>