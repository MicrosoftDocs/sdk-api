---
UID: NF:d2d1.ID2D1Geometry.CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink) (d2d1.h)
description: Combines this geometry with the specified geometry and stores the result in an ID2D1SimplifiedGeometrySink.
helpviewer_keywords: ["CombineWithGeometry","CombineWithGeometry method [Direct2D]","CombineWithGeometry method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","CombineWithGeometry method","ID2D1Geometry.CombineWithGeometry","ID2D1Geometry.CombineWithGeometry(ID2D1Geometry","D2D1_COMBINE_MODE","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","ID2D1Geometry::CombineWithGeometry","ID2D1Geometry::CombineWithGeometry(ID2D1Geometry","D2D1_COMBINE_MODE","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","d2d1/ID2D1Geometry::CombineWithGeometry","direct2d.ID2D1Geometry_CombineWithGeometry_ptr_ID2D1Geometry_D2D1_COMBINE_MODE_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1Geometry_CombineWithGeometry_ptr_ID2D1Geometry_D2D1_COMBINE_MODE_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: 957e9117-9434-4fe6-a93d-986134be7828
ms.date: 12/05/2018
ms.keywords: CombineWithGeometry, CombineWithGeometry method [Direct2D], CombineWithGeometry method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],CombineWithGeometry method, ID2D1Geometry.CombineWithGeometry, ID2D1Geometry.CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), ID2D1Geometry::CombineWithGeometry, ID2D1Geometry::CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), d2d1/ID2D1Geometry::CombineWithGeometry, direct2d.ID2D1Geometry_CombineWithGeometry_ptr_ID2D1Geometry_D2D1_COMBINE_MODE_ref_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink
f1_keywords:
- d2d1/ID2D1Geometry.CombineWithGeometry
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
- ID2D1Geometry.CombineWithGeometry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Combines this geometry with the specified geometry and stores the result in an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.

## -parameters

### -param inputGeometry

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>*</b>

The geometry to combine with this instance.

### -param combineMode

Type: [in] <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_combine_mode">D2D1_COMBINE_MODE</a></b>

The type of combine operation to perform.

### -param inputGeometryTransform

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a> &</b>

The transform to apply to <i>inputGeometry</i> before combining.

### -param geometrySink

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The result of the combine operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>