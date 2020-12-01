---
UID: NF:d2d1effectauthor.ID2D1Transform.MapInputRectsToOutputRect
title: ID2D1Transform::MapInputRectsToOutputRect (d2d1effectauthor.h)
description: Performs the inverse mapping to MapOutputRectToInputRects.
helpviewer_keywords: ["ID2D1Transform interface [Direct2D]","MapInputRectsToOutputRect method","ID2D1Transform.MapInputRectsToOutputRect","ID2D1Transform::MapInputRectsToOutputRect","MapInputRectsToOutputRect","MapInputRectsToOutputRect method [Direct2D]","MapInputRectsToOutputRect method [Direct2D]","ID2D1Transform interface","d2d1effectauthor/ID2D1Transform::MapInputRectsToOutputRect","direct2d.id2d1transform_mapinputrectstooutputrect"]
old-location: direct2d\id2d1transform_mapinputrectstooutputrect.htm
tech.root: Direct2D
ms.assetid: 8FC15A61-767C-460A-A260-9F56A41DA87F
ms.date: 12/05/2018
ms.keywords: ID2D1Transform interface [Direct2D],MapInputRectsToOutputRect method, ID2D1Transform.MapInputRectsToOutputRect, ID2D1Transform::MapInputRectsToOutputRect, MapInputRectsToOutputRect, MapInputRectsToOutputRect method [Direct2D], MapInputRectsToOutputRect method [Direct2D],ID2D1Transform interface, d2d1effectauthor/ID2D1Transform::MapInputRectsToOutputRect, direct2d.id2d1transform_mapinputrectstooutputrect
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Transform::MapInputRectsToOutputRect
 - d2d1effectauthor/ID2D1Transform::MapInputRectsToOutputRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1Transform.MapInputRectsToOutputRect
---

# ID2D1Transform::MapInputRectsToOutputRect


## -description

Performs the inverse mapping to <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects">MapOutputRectToInputRects</a>.

## -parameters

### -param inputRects [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

An array of input rectangles to be mapped to the output rectangle.  The <i>inputRects</i> parameter is always equal to the input bounds.

### -param inputOpaqueSubRects [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

An array of input rectangles to be mapped to the opaque output rectangle.

### -param inputRectCount

Type: <b>UINT32</b>

The number of inputs specified. The implementation guarantees that this is equal to the number of inputs specified on the transform.

### -param outputRect

Type: <b><a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

The output rectangle that maps to the corresponding input rectangle.

### -param outputOpaqueSubRect

Type: <b><a href="/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)">D2D1_RECT_L</a>*</b>

The output rectangle that maps to the corresponding opaque input rectangle.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The transform implementation must ensure that any pixel shader or software callback implementation it provides honors this calculation.

Unlike the <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects">MapOutputRectToInputRects</a> and <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect">MapInvalidRect</a> functions, this method is explicitly called by the renderer at a determined place in its rendering algorithm. The transform implementation may change its state based on the input rectangles and use this information to control its rendering information. This method is always called before the <b>MapInvalidRect</b> and <b>MapOutputRectToInputRects</b> methods of the transform.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl">ID2D1EffectImpl</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>