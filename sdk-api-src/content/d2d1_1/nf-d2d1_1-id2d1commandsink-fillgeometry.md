---
UID: NF:d2d1_1.ID2D1CommandSink.FillGeometry
title: ID2D1CommandSink::FillGeometry (d2d1_1.h)
description: Indicates to the command sink a geometry to be filled.
helpviewer_keywords: ["FillGeometry","FillGeometry method [Direct2D]","FillGeometry method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","FillGeometry method","ID2D1CommandSink.FillGeometry","ID2D1CommandSink::FillGeometry","d2d1_1/ID2D1CommandSink::FillGeometry","direct2d.id2d1commandsink_fillgeometry"]
old-location: direct2d\id2d1commandsink_fillgeometry.htm
tech.root: Direct2D
ms.assetid: 04e93b19-f3a7-4196-bce0-e656d48116ef
ms.date: 12/05/2018
ms.keywords: FillGeometry, FillGeometry method [Direct2D], FillGeometry method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillGeometry method, ID2D1CommandSink.FillGeometry, ID2D1CommandSink::FillGeometry, d2d1_1/ID2D1CommandSink::FillGeometry, direct2d.id2d1commandsink_fillgeometry
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
 - ID2D1CommandSink::FillGeometry
 - d2d1_1/ID2D1CommandSink::FillGeometry
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
 - ID2D1CommandSink.FillGeometry
---

# ID2D1CommandSink::FillGeometry


## -description

Indicates to the command sink a geometry to be filled.

## -parameters

### -param geometry [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry that should be filled.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The primary brush used to fill the geometry.

### -param opacityBrush [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

A brush whose alpha channel is used to modify the opacity of the primary fill brush.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

If the opacity brush is specified, the primary brush will be a bitmap brush fixed on both the x-axis and the y-axis.

Ellipses and rounded rectangles are converted to the corresponding geometry before being passed to <b>FillGeometry</b>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">ID2D1RenderTarget::FillGeometry</a>