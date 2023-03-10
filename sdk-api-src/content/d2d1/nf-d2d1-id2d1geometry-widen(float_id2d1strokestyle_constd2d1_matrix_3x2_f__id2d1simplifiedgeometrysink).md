---
UID: NF:d2d1.ID2D1Geometry.Widen(FLOAT,ID2D1StrokeStyle,constD2D1_MATRIX_3X2_F&,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink) (d2d1.h)
description: Widens the geometry by the specified stroke and writes the result to an ID2D1SimplifiedGeometrySink after it has been transformed by the specified matrix and flattened using the default tolerance. (overload 2/2)
helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","Widen method","ID2D1Geometry.Widen","ID2D1Geometry.Widen(FLOAT","ID2D1StrokeStyle","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","ID2D1Geometry::Widen","ID2D1Geometry::Widen(FLOAT","ID2D1StrokeStyle","const D2D1_MATRIX_3X2_F &","ID2D1SimplifiedGeometrySink)","Widen","Widen method [Direct2D]","Widen method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::Widen","direct2d.ID2D1Geometry_Widen_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1Geometry_Widen_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: 9f316e4d-f167-4c53-81bd-6e1ef6d74eda
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Widen method, ID2D1Geometry.Widen, ID2D1Geometry.Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Widen, ID2D1Geometry::Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), Widen, Widen method [Direct2D], Widen method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Widen, direct2d.ID2D1Geometry_Widen_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry::Widen
 - d2d1/ID2D1Geometry::Widen
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
 - ID2D1Geometry.Widen
---

## -description

Widens the geometry by the specified stroke and writes the result to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> after it has been transformed by the specified matrix and flattened using the default tolerance.

## -parameters

### -param strokeWidth

Type: [in] <b>FLOAT</b>

The amount by which to widen the geometry.

### -param strokeStyle

Type: [in, optional] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply to the geometry, or <b>NULL</b>.

### -param worldTransform

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a> &</b>

The transform to apply to the geometry after widening it.

### -param geometrySink

Type:  [in]<b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> to which the widened geometry is appended.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

