---
UID: NF:d2d1_1.ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,constD2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_DESCRIPTION)
title: ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_DESCRIPTION) (d2d1_1.h)
description: Computes the point that exists at a given distance along the path geometry along with the index of the segment the point is on and the directional vector at that point. (overload 4/4)
old-location: direct2d\id2d1pathgeometry1_computepointandsegmentatlength.htm
tech.root: Direct2D
ms.assetid: 4a47d928-7482-413a-ad9d-e887b309e367
ms.date: 12/05/2018
ms.keywords: ComputePointAndSegmentAtLength, ComputePointAndSegmentAtLength method [Direct2D], ComputePointAndSegmentAtLength method [Direct2D],ID2D1PathGeometry1 interface, ID2D1PathGeometry1 interface [Direct2D],ComputePointAndSegmentAtLength method, ID2D1PathGeometry1.ComputePointAndSegmentAtLength, ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_DESCRIPTION), ID2D1PathGeometry1::ComputePointAndSegmentAtLength, ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_DESCRIPTION), d2d1_1/ID2D1PathGeometry1::ComputePointAndSegmentAtLength, direct2d.id2d1pathgeometry1_computepointandsegmentatlength
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
 - D2d1.dll
api_name:
 - ID2D1PathGeometry1.ComputePointAndSegmentAtLength
---

# ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_DESCRIPTION)


## -description

Computes the point that exists at a given distance along the path geometry along with the index of the segment 
      the point is on and the directional vector at that point.

## -parameters

### -param length

Type: <b>FLOAT</b>

The distance to walk along the path.

### -param startSegment

Type: <b>UINT</b>

The index of the segment at which to begin walking. Note: This index is global to the entire path, not just a particular figure.

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the path prior to walking.

### -param flatteningTolerance

Type: <b>FLOAT</b>

The flattening tolerance to use when walking along an arc or Bezier segment. The flattening tolerance is the maximum 
            error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge 
            from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.

### -param pointDescription [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION</a>*</b>

When this method returns, contains a description of the point that can be found at the given location.

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
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One of the inputs was in an invalid range.</td>
</tr>
</table>

## -remarks

A <i>length</i> that is less than 0 or is not a number is treated as if it were 0.

If <i>length</i> is greater than the total length of the path, then the end point of the path is returned.

<h3><a id="Example_Illustration"></a><a id="example_illustration"></a><a id="EXAMPLE_ILLUSTRATION"></a>Example Illustration</h3>
Consider this example that explains the value of different parameters returned for the given path geometry. 

<img alt="A diagram of a path geometry and its lengths." src="images/computepointandsegmentatlength.png"/>
Here are two different scenarios.

<h3><a id="You_want_to_retrieve_the_segment_at_a_length_L2"></a><a id="you_want_to_retrieve_the_segment_at_a_length_l2"></a><a id="YOU_WANT_TO_RETRIEVE_THE_SEGMENT_AT_A_LENGTH_L2"></a>You want to retrieve the segment at a length L2</h3>
You call ComputePointAndSegmentAtLength(Length = L2, startSegment =0). The API returns the following:


<ul>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::point</a>  = p2.</li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::endSegment </a>= 3 (segment DE). This is the value you want.</li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::lengthToEndSegment</a> = length (AD).
</li>
</ul>
<h3><a id="You_wants_to_improve_the_performance_of_calculating_a_point_at_a_given_length_for_animating_along_a_path"></a><a id="you_wants_to_improve_the_performance_of_calculating_a_point_at_a_given_length_for_animating_along_a_path"></a><a id="YOU_WANTS_TO_IMPROVE_THE_PERFORMANCE_OF_CALCULATING_A_POINT_AT_A_GIVEN_LENGTH_FOR_ANIMATING_ALONG_A_PATH"></a>You wants to improve the performance of calculating a point at a given length for animating along a path</h3>
Normally, the time intervals would be small and regular, resulting in many animation points per segment. For the purposes of demonstration, however, we will assume the you query ComputePointAndSegmentAtLength three times, with irregularly-spaced lengths L1, L2, L3:

You call ComputePointAndSegmentAtLength(Length = L1, startSegment = 0). The API returns the following:


<ul>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::point</a>  = P1.</li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::endSegment</a> = 1 (segment BC). </li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::lengthToEndSegment</a> = length (AB).
</li>
</ul>
You call ComputePointAndSegmentAtLength(Length = L2 - Length(AB), startSegment = 1). The API returns the following:


<ul>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::point</a>  = P2.</li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::endSegment </a>= 3 (segment DE). </li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::lengthToEndSegment</a> = length (AD).
</li>
</ul>
You call ComputePointAndSegmentAtLength(= L3-length(AB)-length(BD), startSegment = 3). The API returns the following:


<ul>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::point</a>  = P3.</li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::endSegment </a>= 3 (segment DE). </li>
<li>
<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION::lengthToEndSegment</a> =0.
</li>
</ul>

## -see-also

<a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>



<a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>



<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_point_description">D2D1_POINT_DESCRIPTION</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1">ID2D1PathGeometry1</a>
