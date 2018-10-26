---
UID: NF:d2d1_1.ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F &,D2D1_POINT_DESCRIPTION)
title: ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F &,D2D1_POINT_DESCRIPTION)
author: windows-sdk-content
description: Computes the point that exists at a given distance along the path geometry along with the index of the segment the point is on and the directional vector at that point.
old-location: direct2d\id2d1pathgeometry1_computepointandsegmentatlength_4.htm
tech.root: direct2d
ms.assetid: 03921E25-BC5A-425B-8D65-3FC0EAA8E0AD
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ComputePointAndSegmentAtLength, ComputePointAndSegmentAtLength method [Direct2D], ComputePointAndSegmentAtLength method [Direct2D],ID2D1PathGeometry1 interface, ID2D1PathGeometry1 interface [Direct2D],ComputePointAndSegmentAtLength method, ID2D1PathGeometry1.ComputePointAndSegmentAtLength, ID2D1PathGeometry1.ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F &,D2D1_POINT_DESCRIPTION), ID2D1PathGeometry1::ComputePointAndSegmentAtLength, ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F &,D2D1_POINT_DESCRIPTION), d2d1_3/ID2D1PathGeometry1::ComputePointAndSegmentAtLength, direct2d.id2d1pathgeometry1_computepointandsegmentatlength_4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1PathGeometry1.ComputePointAndSegmentAtLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PathGeometry1::ComputePointAndSegmentAtLength(FLOAT,UINT32,const D2D1_MATRIX_3X2_F &,D2D1_POINT_DESCRIPTION)


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


### -param worldTransform [ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transform to apply to the path prior to walking.


### -param pointDescription [out]

Type: <b><a href="https://msdn.microsoft.com/d6e7a4c1-135f-4ffe-91d7-486de8a9338d">D2D1_POINT_DESCRIPTION</a>*</b>

When this method returns, contains a description of the point that can be found at the given location.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

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




<a href="https://msdn.microsoft.com/21f0a4a3-3c6c-434d-8cfc-767c7654849e">ID2D1PathGeometry1</a>
 

 

