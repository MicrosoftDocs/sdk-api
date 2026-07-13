---
UID: NF:d2d1_1.ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,constD2D1_MATRIX_3X2_F,D2D1_POINT_DESCRIPTION)
title: ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,D2D1_POINT_DESCRIPTION) (d2d1_1.h)
description: Computes the point that exists at a given distance along the path geometry along with the index of the segment the point is on and the directional vector at that point. (overload 2/4)
helpviewer_keywords: ["ComputePointAndSegmentAtLength","ComputePointAndSegmentAtLength method [Direct2D]","ComputePointAndSegmentAtLength method [Direct2D]","ID2D1PathGeometry1 interface","ID2D1PathGeometry1 interface [Direct2D]","ComputePointAndSegmentAtLength method","ID2D1PathGeometry1.ComputePointAndSegmentAtLength","ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT","UINT32","const D2D1_MATRIX_3X2_F","D2D1_POINT_DESCRIPTION)","ID2D1PathGeometry1::ComputePointAndSegmentAtLength","ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT","UINT32","const D2D1_MATRIX_3X2_F","D2D1_POINT_DESCRIPTION)","d2d1_3/ID2D1PathGeometry1::ComputePointAndSegmentAtLength","direct2d.id2d1pathgeometry1_computepointandsegmentatlength_3"]
old-location: direct2d\id2d1pathgeometry1_computepointandsegmentatlength_3.htm
tech.root: Direct2D
ms.assetid: EF383415-1A5F-4D1F-BB31-5D920A42F8AF
ms.date: 12/05/2018
ms.keywords: ComputePointAndSegmentAtLength, ComputePointAndSegmentAtLength method [Direct2D], ComputePointAndSegmentAtLength method [Direct2D],ID2D1PathGeometry1 interface, ID2D1PathGeometry1 interface [Direct2D],ComputePointAndSegmentAtLength method, ID2D1PathGeometry1.ComputePointAndSegmentAtLength, ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,D2D1_POINT_DESCRIPTION), ID2D1PathGeometry1::ComputePointAndSegmentAtLength, ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,D2D1_POINT_DESCRIPTION), d2d1_3/ID2D1PathGeometry1::ComputePointAndSegmentAtLength, direct2d.id2d1pathgeometry1_computepointandsegmentatlength_3
req.header: d2d1_1.h
req.include-header: D2d1_1.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1PathGeometry1::ComputePointAndSegmentAtLength
 - d2d1_1/ID2D1PathGeometry1::ComputePointAndSegmentAtLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1PathGeometry1.ComputePointAndSegmentAtLength
---

# ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,D2D1_POINT_DESCRIPTION)


## -description

Computes the point that exists at a given distance along the path geometry along with the index of the segment
          the point is on and the directional vector at that point.

## -parameters

### -param length

Type: <b>FLOAT</b>

The distance to walk along the path.

### -param startSegment

Type: <b>UINT32</b>

The index of the segment at which to begin walking. Note: This index is global to the entire path, not just a particular figure.

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the path prior to walking.

### -param pointDescription [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION</a>*</b>

When this method returns, contains a description of the point that can be found at the given location.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

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
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One of the inputs was in an invalid range.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1">ID2D1PathGeometry1</a>
