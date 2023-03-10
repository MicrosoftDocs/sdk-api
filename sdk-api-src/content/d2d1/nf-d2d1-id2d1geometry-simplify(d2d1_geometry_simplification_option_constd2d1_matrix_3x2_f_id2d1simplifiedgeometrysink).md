---
UID: NF:d2d1.ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,constD2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink) (d2d1.h)
description: Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an ID2D1SimplifiedGeometrySink. (overload 3/4)
helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","Simplify method","ID2D1Geometry.Simplify","ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION","const D2D1_MATRIX_3X2_F","ID2D1SimplifiedGeometrySink)","ID2D1Geometry::Simplify","ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION","const D2D1_MATRIX_3X2_F","ID2D1SimplifiedGeometrySink)","Simplify","Simplify method [Direct2D]","Simplify method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::Simplify","direct2d.ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: c59677bf-dbcc-403a-b86f-eb1531365fa4
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Simplify method, ID2D1Geometry.Simplify, ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Simplify, ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink), Simplify, Simplify method [Direct2D], Simplify method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Simplify, direct2d.ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry::Simplify
 - d2d1/ID2D1Geometry::Simplify
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
 - ID2D1Geometry.Simplify
---

## -description

Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.

## -parameters

### -param simplificationOption

Type: [in] <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option">D2D1_GEOMETRY_SIMPLIFICATION_OPTION</a></b>

A value that specifies whether the simplified geometry should contain curves.

### -param worldTransform

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the simplified geometry.

### -param geometrySink

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> to which the simplified geometry is appended.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

