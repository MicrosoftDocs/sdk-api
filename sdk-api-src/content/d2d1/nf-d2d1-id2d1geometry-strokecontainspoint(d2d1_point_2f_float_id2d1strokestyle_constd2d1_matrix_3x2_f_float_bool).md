---
UID: NF:d2d1.ID2D1Geometry.StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,constD2D1_MATRIX_3X2_F,FLOAT,BOOL)
title: ID2D1Geometry::StrokeContainsPoint (d2d1.h)
description: Determines whether the geometry's stroke contains the specified point given the specified stroke thickness, style, and transform.
helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","StrokeContainsPoint method","ID2D1Geometry.StrokeContainsPoint","ID2D1Geometry::StrokeContainsPoint","ID2D1Geometry::StrokeContainsPoint(D2D1_POINT_2F","FLOAT","ID2D1StrokeStyle","const D2D1_MATRIX_3X2_F &","FLOAT","BOOL)","StrokeContainsPoint","StrokeContainsPoint method [Direct2D]","StrokeContainsPoint method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::StrokeContainsPoint","direct2d.ID2D1Geometry_StrokeContainsPoint_D2D_POINT_2F_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_BOOL"]
old-location: direct2d\ID2D1Geometry_StrokeContainsPoint_D2D_POINT_2F_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_BOOL.htm
tech.root: Direct2D
ms.assetid: 5a031834-dc27-44f6-8344-0aa6958eff75
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],StrokeContainsPoint method, ID2D1Geometry.StrokeContainsPoint, ID2D1Geometry::StrokeContainsPoint, ID2D1Geometry::StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,FLOAT,BOOL), StrokeContainsPoint, StrokeContainsPoint method [Direct2D], StrokeContainsPoint method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::StrokeContainsPoint, direct2d.ID2D1Geometry_StrokeContainsPoint_D2D_POINT_2F_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_BOOL
f1_keywords:
- d2d1/ID2D1Geometry.StrokeContainsPoint
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
- ID2D1Geometry.StrokeContainsPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Determines whether the geometry's stroke contains the specified point given the specified stroke thickness, style, and transform.

## -parameters

### -param point

Type: [in] <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point to test for containment.

### -param strokeWidth

Type: [in] <b>FLOAT</b>

The thickness of the stroke to apply.

### -param strokeStyle

Type: [in, optional] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply.

### -param worldTransform

Type: [in, optional] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the stroked geometry. 

### -param flatteningTolerance

Type: [in] <b>FLOAT</b>

The numeric accuracy with which the precise geometric path and path intersection is calculated. Points missing the stroke by less than the tolerance are still considered inside. Smaller values produce more accurate results but cause slower execution.

### -param contains

Type: [out] <b>BOOL*</b>

When this method returns, contains a boolean value set to true if the geometry's stroke contains the specified point; otherwise, false. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
