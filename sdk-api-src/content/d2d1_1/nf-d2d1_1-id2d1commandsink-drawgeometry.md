---
UID: NF:d2d1_1.ID2D1CommandSink.DrawGeometry
title: ID2D1CommandSink::DrawGeometry (d2d1_1.h)
description: Indicates the geometry to be drawn to the command sink.
helpviewer_keywords: ["DrawGeometry","DrawGeometry method [Direct2D]","DrawGeometry method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawGeometry method","ID2D1CommandSink.DrawGeometry","ID2D1CommandSink::DrawGeometry","d2d1_1/ID2D1CommandSink::DrawGeometry","direct2d.id2d1commandsink_drawgeometry"]
old-location: direct2d\id2d1commandsink_drawgeometry.htm
tech.root: Direct2D
ms.assetid: ff91dd6c-0604-44aa-a30c-6b531cc3fb58
ms.date: 12/05/2018
ms.keywords: DrawGeometry, DrawGeometry method [Direct2D], DrawGeometry method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawGeometry method, ID2D1CommandSink.DrawGeometry, ID2D1CommandSink::DrawGeometry, d2d1_1/ID2D1CommandSink::DrawGeometry, direct2d.id2d1commandsink_drawgeometry
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
 - ID2D1CommandSink::DrawGeometry
 - d2d1_1/ID2D1CommandSink::DrawGeometry
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
 - ID2D1CommandSink.DrawGeometry
---

# ID2D1CommandSink::DrawGeometry


## -description

Indicates the geometry to be drawn to the command sink.

## -parameters

### -param geometry [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry </a>*</b>

The geometry to be stroked.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush that will be used to fill the stroked geometry.

### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of the stroke.

## -returns

Type: <b>HRESULT</b>

An HRESULT.

## -remarks

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1ellipsegeometry">Ellipses</a> and <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">rounded rectangles</a> are converted to the corresponding ellipse and rounded rectangle geometries before calling into the <b>DrawGeometry</b> method.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry">ID2D1RenderTarget::DrawGeometry</a>