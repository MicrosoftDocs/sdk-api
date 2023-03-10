---
UID: NF:d2d1.ID2D1Geometry.ComputePointAtLength(FLOAT,constD2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_2F,D2D1_POINT_2F)
title: ID2D1Geometry::ComputePointAtLength (d2d1.h)
description: Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance. (overload 1/2)
helpviewer_keywords: ["ComputePointAtLength","ComputePointAtLength method [Direct2D]","ComputePointAtLength method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","ComputePointAtLength method","ID2D1Geometry.ComputePointAtLength","ID2D1Geometry::ComputePointAtLength","ID2D1Geometry::ComputePointAtLength(FLOAT","const D2D1_MATRIX_3X2_F","FLOAT","D2D1_POINT_2F","D2D1_POINT_2F)","d2d1/ID2D1Geometry::ComputePointAtLength","direct2d.ID2D1Geometry_ComputePointAtLength_FLOAT_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_D2D_POINT_2F_ptr_D2D_POINT_2F"]
old-location: direct2d\ID2D1Geometry_ComputePointAtLength_FLOAT_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_D2D_POINT_2F_ptr_D2D_POINT_2F.htm
tech.root: Direct2D
ms.assetid: ae611265-4b0b-476e-afc5-23bb5a0cff26
ms.date: 12/05/2018
ms.keywords: ComputePointAtLength, ComputePointAtLength method [Direct2D], ComputePointAtLength method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],ComputePointAtLength method, ID2D1Geometry.ComputePointAtLength, ID2D1Geometry::ComputePointAtLength, ID2D1Geometry::ComputePointAtLength(FLOAT,const D2D1_MATRIX_3X2_F,FLOAT,D2D1_POINT_2F,D2D1_POINT_2F), d2d1/ID2D1Geometry::ComputePointAtLength, direct2d.ID2D1Geometry_ComputePointAtLength_FLOAT_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_D2D_POINT_2F_ptr_D2D_POINT_2F
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Geometry::ComputePointAtLength
 - d2d1/ID2D1Geometry::ComputePointAtLength
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
 - ID2D1Geometry.ComputePointAtLength
---

## -description

Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.

## -parameters

### -param length

Type: [in] <b>FLOAT</b>

The distance along the geometry of the point and tangent to find. If this distance is less than 0, this method calculates the first point in the geometry. If this distance is greater than the length of the geometry, this method calculates the last point in the geometry.

### -param worldTransform

Type: [in, optional] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry before calculating the specified point and tangent, or <b>NULL</b>.

### -param flatteningTolerance

Type: [in] <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.

### -param point

Type: [out, optional] <b><a href="/windows/win32/api/dcommon/ns-dcommon-d2d_point_2f">D2D1_POINT_2F</a>*</b>

The location at the specified distance along the geometry. If the geometry is empty,  this point contains NaN as its x and y values.

### -param unitTangentVector

Type: [out, optional] <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a>*</b>

When this method returns, contains a pointer to the tangent vector at the specified distance along the geometry. If the geometry is empty, this vector contains NaN as its x and y values. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

