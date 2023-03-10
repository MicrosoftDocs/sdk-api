---
UID: NF:d2d1.ID2D1Geometry.CompareWithGeometry(ID2D1Geometry,constD2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION)
title: ID2D1Geometry::CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION) (d2d1.h)
description: Describes the intersection between this geometry and the specified geometry. The comparison is performed using the default flattening tolerance. (overload 2/2)
helpviewer_keywords: ["CompareWithGeometry","CompareWithGeometry method [Direct2D]","CompareWithGeometry method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","CompareWithGeometry method","ID2D1Geometry.CompareWithGeometry","ID2D1Geometry.CompareWithGeometry(ID2D1Geometry","const D2D1_MATRIX_3X2_F","D2D1_GEOMETRY_RELATION)","ID2D1Geometry::CompareWithGeometry","ID2D1Geometry::CompareWithGeometry(ID2D1Geometry","const D2D1_MATRIX_3X2_F","D2D1_GEOMETRY_RELATION)","d2d1/ID2D1Geometry::CompareWithGeometry","direct2d.ID2D1Geometry_CompareWithGeometry_ptr_ID2D1Geometry_ptr_D2D_MATRIX_3X2_F_ptr_D2D1_GEOMETRY_RELATION"]
old-location: direct2d\ID2D1Geometry_CompareWithGeometry_ptr_ID2D1Geometry_ptr_D2D_MATRIX_3X2_F_ptr_D2D1_GEOMETRY_RELATION.htm
tech.root: Direct2D
ms.assetid: 49887b1a-24ca-4c1c-8c70-b53a995028fd
ms.date: 12/05/2018
ms.keywords: CompareWithGeometry, CompareWithGeometry method [Direct2D], CompareWithGeometry method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],CompareWithGeometry method, ID2D1Geometry.CompareWithGeometry, ID2D1Geometry.CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION), ID2D1Geometry::CompareWithGeometry, ID2D1Geometry::CompareWithGeometry(ID2D1Geometry,const D2D1_MATRIX_3X2_F,D2D1_GEOMETRY_RELATION), d2d1/ID2D1Geometry::CompareWithGeometry, direct2d.ID2D1Geometry_CompareWithGeometry_ptr_ID2D1Geometry_ptr_D2D_MATRIX_3X2_F_ptr_D2D1_GEOMETRY_RELATION
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
 - ID2D1Geometry::CompareWithGeometry
 - d2d1/ID2D1Geometry::CompareWithGeometry
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
 - ID2D1Geometry.CompareWithGeometry
---

## -description

Describes the intersection between this geometry and the specified geometry. The comparison is performed using the default flattening tolerance.

## -parameters

### -param inputGeometry

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry to test.

### -param inputGeometryTransform

Type: [in, optional] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to <i>inputGeometry</i>, or <b>NULL</b>.

### -param relation

Type: [out] <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_geometry_relation">D2D1_GEOMETRY_RELATION</a>*</b>

When this method returns, contains a pointer to a value that describes how this geometry is related to <i>inputGeometry</i>. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

When interpreting the returned <i>relation</i> value, it is important to remember that the member <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_geometry_relation">D2D1_GEOMETRY_RELATION_IS_CONTAINED</a> of the  <b>D2D1_GEOMETRY_RELATION</b> enumeration type means that this geometry is contained  inside <i>inputGeometry</i>, not that this geometry contains <i>inputGeometry</i>. 

For  more information about how to interpret other possible return values, see <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_geometry_relation">D2D1_GEOMETRY_RELATION</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

