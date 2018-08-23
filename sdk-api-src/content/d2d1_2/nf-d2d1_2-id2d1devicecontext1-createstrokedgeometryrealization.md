---
UID: NF:d2d1_2.ID2D1DeviceContext1.CreateStrokedGeometryRealization
title: ID2D1DeviceContext1::CreateStrokedGeometryRealization
author: windows-sdk-content
description: Creates a device-dependent representation of the stroke of a geometry that can be subsequently rendered.
old-location: direct2d\id2d1devicecontext1_createstrokedgeometryrealization.htm
old-project: direct2d
ms.assetid: 455EE223-4CEA-4FBA-8885-B0BA6B465C05
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateStrokedGeometryRealization, CreateStrokedGeometryRealization method [Direct2D], CreateStrokedGeometryRealization method [Direct2D],ID2D1DeviceContext1 interface, ID2D1DeviceContext1 interface [Direct2D],CreateStrokedGeometryRealization method, ID2D1DeviceContext1.CreateStrokedGeometryRealization, ID2D1DeviceContext1::CreateStrokedGeometryRealization, d2d1_2/ID2D1DeviceContext1::CreateStrokedGeometryRealization, direct2d.id2d1devicecontext1_createstrokedgeometryrealization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1_2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_RENDERING_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext1.CreateStrokedGeometryRealization
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ID2D1DeviceContext1::CreateStrokedGeometryRealization


## -description


Creates a device-dependent representation of the stroke of a geometry that can be subsequently rendered.


## -parameters




### -param geometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry to realize.


### -param flatteningTolerance

Type: <b>FLOAT </b>

The flattening tolerance to use when converting Beziers to line segments. This parameter shares the same units as the coordinates of the geometry.


### -param strokeWidth

Type: <b>FLOAT </b>

The width of the stroke. This parameter shares the same units as the coordinates of the geometry.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The stroke style (optional).


### -param geometryRealization [out]

Type: <b><a href="https://msdn.microsoft.com/EC2CF78B-5CED-494A-9ED3-407A4B6CD113">ID2D1GeometryRealization</a>**</b>

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



This method is used in conjunction with <a href="https://msdn.microsoft.com/BA4FB8E7-E59A-42BD-86BB-8048267A26AA">ID2D1DeviceContext1::DrawGeometryRealization</a>. The <a href="https://msdn.microsoft.com/62461D91-FAAF-4ABC-A852-6CD4B9B8182B">D2D1::ComputeFlatteningTolerance</a> helper API may be used to determine the proper flattening tolerance.

If the provided stroke style specifies a stroke transform type other than <a href="https://msdn.microsoft.com/99c2c5c8-49ce-4865-befa-e9f92905a260">D2D1_STROKE_TRANSFORM_TYPE_NORMAL</a>, then the stroke will be realized assuming the identity transform and a DPI of 96.




## -see-also




<a href="https://msdn.microsoft.com/E08FDAE4-05D3-472C-9AD9-228BAF989F1D">ID2D1DeviceContext1</a>
 

 

