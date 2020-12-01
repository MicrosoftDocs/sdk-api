---
UID: NF:d2d1_2.ID2D1DeviceContext1.DrawGeometryRealization
title: ID2D1DeviceContext1::DrawGeometryRealization (d2d1_2.h)
description: Renders a given geometry realization to the target with the specified brush.
helpviewer_keywords: ["DrawGeometryRealization","DrawGeometryRealization method [Direct2D]","DrawGeometryRealization method [Direct2D]","ID2D1DeviceContext1 interface","ID2D1DeviceContext1 interface [Direct2D]","DrawGeometryRealization method","ID2D1DeviceContext1.DrawGeometryRealization","ID2D1DeviceContext1::DrawGeometryRealization","d2d1_2/ID2D1DeviceContext1::DrawGeometryRealization","direct2d.id2d1devicecontext1_drawgeometryrealization"]
old-location: direct2d\id2d1devicecontext1_drawgeometryrealization.htm
tech.root: Direct2D
ms.assetid: BA4FB8E7-E59A-42BD-86BB-8048267A26AA
ms.date: 12/05/2018
ms.keywords: DrawGeometryRealization, DrawGeometryRealization method [Direct2D], DrawGeometryRealization method [Direct2D],ID2D1DeviceContext1 interface, ID2D1DeviceContext1 interface [Direct2D],DrawGeometryRealization method, ID2D1DeviceContext1.DrawGeometryRealization, ID2D1DeviceContext1::DrawGeometryRealization, d2d1_2/ID2D1DeviceContext1::DrawGeometryRealization, direct2d.id2d1devicecontext1_drawgeometryrealization
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext1::DrawGeometryRealization
 - d2d1_2/ID2D1DeviceContext1::DrawGeometryRealization
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
 - ID2D1DeviceContext1.DrawGeometryRealization
---

# ID2D1DeviceContext1::DrawGeometryRealization


## -description

Renders a given geometry realization to the target with the specified brush.

## -parameters

### -param geometryRealization [in]

Type: <b><a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization">ID2D1GeometryRealization</a>*</b>

The geometry realization to be rendered.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush to render the realization with.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.
                </td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -remarks

This method respects all currently set state (transform, DPI, unit mode, target image, clips, layers); 
        however, artifacts such as faceting may appear when rendering the realizations with a large effective scale (either via the transform or the DPI). 
        Callers should create their realizations with an appropriate flattening tolerance using either <a href="/windows/desktop/Direct2D/direct2d-constants">D2D1_DEFAULT_FLATTENING_TOLERANCE</a> 
        or <a href="/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)">ComputeFlatteningTolerance</a> to compensate for this.
      

Additionally, callers should be aware of the safe render bounds when creating geometry realizations. 
      If a geometry extends outside of [-524,287, 524,287] DIPs in either the X- or the Y- direction in its original (pre-transform) coordinate space, 
      then it may be clipped to those bounds when it is realized. This clipping will be visible even if the realization is subsequently transformed to fit within the safe render bounds.

## -see-also

<a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1">ID2D1DeviceContext1</a>