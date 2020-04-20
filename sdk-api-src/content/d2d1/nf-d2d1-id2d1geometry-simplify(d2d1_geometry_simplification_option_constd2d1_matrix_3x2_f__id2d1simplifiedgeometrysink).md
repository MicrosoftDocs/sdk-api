---
UID: NF:d2d1.ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink) (d2d1.h)
description: Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an ID2D1SimplifiedGeometrySink.helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","Simplify method","ID2D1Geometry.Simplify","ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","ID2D1Geometry::Simplify","ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","Simplify","Simplify method [Direct2D]","Simplify method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::Simplify","direct2d.ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: 46f591e7-a039-4ad3-891d-615554b1d710
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Simplify method, ID2D1Geometry.Simplify, ID2D1Geometry.Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Simplify, ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), Simplify, Simplify method [Direct2D], Simplify method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Simplify, direct2d.ID2D1Geometry_Simplify_D2D1_GEOMETRY_SIMPLIFICATION_OPTION_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink
f1_keywords:
- d2d1/ID2D1Geometry.Simplify
dev_langs:
- c++
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
- ID2D1Geometry.Simplify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry::Simplify(D2D1_GEOMETRY_SIMPLIFICATION_OPTION,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)


## -description


Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.


## -parameters




### -param simplificationOption

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option">D2D1_GEOMETRY_SIMPLIFICATION_OPTION</a></b>

A value that specifies whether the simplified geometry should contain curves.


### -param worldTransform [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the simplified geometry, or <b>NULL</b>.


### -param geometrySink [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> to which the simplified geometry is appended. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

