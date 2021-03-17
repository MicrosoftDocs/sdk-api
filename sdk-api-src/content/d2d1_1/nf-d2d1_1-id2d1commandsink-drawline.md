---
UID: NF:d2d1_1.ID2D1CommandSink.DrawLine
title: ID2D1CommandSink::DrawLine (d2d1_1.h)
description: Draws a line drawn between two points.
helpviewer_keywords: ["DrawLine","DrawLine method [Direct2D]","DrawLine method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","DrawLine method","ID2D1CommandSink.DrawLine","ID2D1CommandSink::DrawLine","d2d1_1/ID2D1CommandSink::DrawLine","direct2d.id2d1commandsink_drawline"]
old-location: direct2d\id2d1commandsink_drawline.htm
tech.root: Direct2D
ms.assetid: 3c47b5af-d258-42f8-b329-eb28d9485d3a
ms.date: 12/05/2018
ms.keywords: DrawLine, DrawLine method [Direct2D], DrawLine method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawLine method, ID2D1CommandSink.DrawLine, ID2D1CommandSink::DrawLine, d2d1_1/ID2D1CommandSink::DrawLine, direct2d.id2d1commandsink_drawline
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
 - ID2D1CommandSink::DrawLine
 - d2d1_1/ID2D1CommandSink::DrawLine
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
 - ID2D1CommandSink.DrawLine
---

# ID2D1CommandSink::DrawLine


## -description

Draws a line drawn between two points.

## -parameters

### -param point0

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The start point of the line.

### -param point1

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point of the line.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to fill the line.

### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke to fill the line.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of the stroke. If not specified, the stroke is solid.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawline">ID2D1RenderTarget::DrawLine</a>