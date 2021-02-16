---
UID: NF:d2d1_2.ID2D1DeviceContext1.CreateStrokedGeometryRealization
title: ID2D1DeviceContext1::CreateStrokedGeometryRealization (d2d1_2.h)
description: Creates a device-dependent representation of the stroke of a geometry that can be subsequently rendered.
helpviewer_keywords: ["CreateStrokedGeometryRealization","CreateStrokedGeometryRealization method [Direct2D]","CreateStrokedGeometryRealization method [Direct2D]","ID2D1DeviceContext1 interface","ID2D1DeviceContext1 interface [Direct2D]","CreateStrokedGeometryRealization method","ID2D1DeviceContext1.CreateStrokedGeometryRealization","ID2D1DeviceContext1::CreateStrokedGeometryRealization","d2d1_2/ID2D1DeviceContext1::CreateStrokedGeometryRealization","direct2d.id2d1devicecontext1_createstrokedgeometryrealization"]
old-location: direct2d\id2d1devicecontext1_createstrokedgeometryrealization.htm
tech.root: Direct2D
ms.assetid: 455EE223-4CEA-4FBA-8885-B0BA6B465C05
ms.date: 12/05/2018
ms.keywords: CreateStrokedGeometryRealization, CreateStrokedGeometryRealization method [Direct2D], CreateStrokedGeometryRealization method [Direct2D],ID2D1DeviceContext1 interface, ID2D1DeviceContext1 interface [Direct2D],CreateStrokedGeometryRealization method, ID2D1DeviceContext1.CreateStrokedGeometryRealization, ID2D1DeviceContext1::CreateStrokedGeometryRealization, d2d1_2/ID2D1DeviceContext1::CreateStrokedGeometryRealization, direct2d.id2d1devicecontext1_createstrokedgeometryrealization
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
 - ID2D1DeviceContext1::CreateStrokedGeometryRealization
 - d2d1_2/ID2D1DeviceContext1::CreateStrokedGeometryRealization
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
 - ID2D1DeviceContext1.CreateStrokedGeometryRealization
---

# ID2D1DeviceContext1::CreateStrokedGeometryRealization


## -description

Creates a device-dependent representation of the stroke of a geometry that can be subsequently rendered.

## -parameters

### -param geometry [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry to realize.

### -param flatteningTolerance

Type: <b>FLOAT </b>

The flattening tolerance to use when converting Beziers to line segments. This parameter shares the same units as the coordinates of the geometry.

### -param strokeWidth

Type: <b>FLOAT </b>

The width of the stroke. This parameter shares the same units as the coordinates of the geometry.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The stroke style (optional).

### -param geometryRealization [out]

Type: <b><a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization">ID2D1GeometryRealization</a>**</b>

When this method returns, contains the address of a pointer to a new geometry realization object.

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
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -remarks

This method is used in conjunction with <a href="/windows/desktop/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization">ID2D1DeviceContext1::DrawGeometryRealization</a>. The <a href="/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)">D2D1::ComputeFlatteningTolerance</a> helper API may be used to determine the proper flattening tolerance.

If the provided stroke style specifies a stroke transform type other than <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_stroke_transform_type">D2D1_STROKE_TRANSFORM_TYPE_NORMAL</a>, then the stroke will be realized assuming the identity transform and a DPI of 96.

## -see-also

<a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1">ID2D1DeviceContext1</a>