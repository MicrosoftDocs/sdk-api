---
UID: NF:d2d1.ID2D1Geometry.ComputePointAtLength
title: ID2D1Geometry::ComputePointAtLength
author: windows-sdk-content
description: Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.
old-location: direct2d\ID2D1Geometry_ComputePointAtLength_FLOAT_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_D2D_POINT_2F_ptr_D2D_POINT_2F.htm
tech.root: direct2d
ms.assetid: ae611265-4b0b-476e-afc5-23bb5a0cff26
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComputePointAtLength, ComputePointAtLength method [Direct2D], ComputePointAtLength method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],ComputePointAtLength method, ID2D1Geometry.ComputePointAtLength, ID2D1Geometry::ComputePointAtLength, ID2D1Geometry::ComputePointAtLength(FLOAT,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_2F,D2D1_POINT_2F), d2d1/ID2D1Geometry::ComputePointAtLength, direct2d.ID2D1Geometry_ComputePointAtLength_FLOAT_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_D2D_POINT_2F_ptr_D2D_POINT_2F
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Geometry.ComputePointAtLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::ComputePointAtLength


## -description


Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.


## -parameters




### -param length

Type: <b>FLOAT</b>

The distance along the geometry of the point and tangent to find. If this distance is less then 0, this method calculates the first point in the geometry. If this distance is greater than the length of the geometry, this method calculates the last point in the geometry.


### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry before calculating the specified point and tangent, or <b>NULL</b>.


### -param flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.


### -param point [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2ee55d63-594b-482d-9e31-2378369c6c30">D2D1_POINT_2F</a>*</b>

The location at the specified distance along the geometry. If the geometry is empty,  this point contains NaN as its x and y values.


### -param unitTangentVector [out, optional]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

When this method returns, contains a pointer to the tangent vector at the specified distance along the geometry. If the geometry is empty,  this vector contains NaN as its x and y values. You must allocate storage for this parameter.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

