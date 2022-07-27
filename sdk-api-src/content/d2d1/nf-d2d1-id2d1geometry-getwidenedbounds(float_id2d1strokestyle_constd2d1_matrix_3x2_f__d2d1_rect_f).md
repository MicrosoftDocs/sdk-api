---
UID: NF:d2d1.ID2D1Geometry.GetWidenedBounds(FLOAT,ID2D1StrokeStyle,constD2D1_MATRIX_3X2_F&,D2D1_RECT_F)
title: ID2D1Geometry::GetWidenedBounds(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,D2D1_RECT_F) (d2d1.h)
description: Gets the bounds of the geometry after it has been widened by the specified stroke width and style and transformed by the specified matrix. (overload 4/4)
helpviewer_keywords: ["GetWidenedBounds","GetWidenedBounds method [Direct2D]","GetWidenedBounds method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","GetWidenedBounds method","ID2D1Geometry.GetWidenedBounds","ID2D1Geometry.GetWidenedBounds(FLOAT","ID2D1StrokeStyle","const D2D1_MATRIX_3X2_F &","D2D1_RECT_F)","ID2D1Geometry::GetWidenedBounds","ID2D1Geometry::GetWidenedBounds(FLOAT","ID2D1StrokeStyle","const D2D1_MATRIX_3X2_F &","D2D1_RECT_F)","d2d1/ID2D1Geometry::GetWidenedBounds","direct2d.ID2D1Geometry_GetWidenedBounds_FLOAT_ptr_ID2D1StrokeStyle_ref_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F"]
old-location: direct2d\ID2D1Geometry_GetWidenedBounds_FLOAT_ptr_ID2D1StrokeStyle_ref_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F.htm
tech.root: Direct2D
ms.assetid: 02f27bcd-8d00-4ae7-a498-98052254b56d
ms.date: 12/05/2018
ms.keywords: GetWidenedBounds, GetWidenedBounds method [Direct2D], GetWidenedBounds method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],GetWidenedBounds method, ID2D1Geometry.GetWidenedBounds, ID2D1Geometry.GetWidenedBounds(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,D2D1_RECT_F), ID2D1Geometry::GetWidenedBounds, ID2D1Geometry::GetWidenedBounds(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,D2D1_RECT_F), d2d1/ID2D1Geometry::GetWidenedBounds, direct2d.ID2D1Geometry_GetWidenedBounds_FLOAT_ptr_ID2D1StrokeStyle_ref_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F
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
 - ID2D1Geometry::GetWidenedBounds
 - d2d1/ID2D1Geometry::GetWidenedBounds
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
 - ID2D1Geometry.GetWidenedBounds
---

# ID2D1Geometry::GetWidenedBounds(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,D2D1_RECT_F)


## -description

Gets the bounds of the geometry after it has been widened by the specified stroke width and style and transformed by the specified matrix.

## -parameters

### -param strokeWidth

Type: <b>FLOAT</b>

The amount by which to widen the geometry by stroking its outline.

### -param strokeStyle [in, optional]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>*</b>

The style of the stroke that widens the geometry.

### -param worldTransform [ref]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

A transform to apply to the geometry after the geometry is transformed and after the geometry has been stroked.

### -param bounds [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

When this method returns, contains the bounds of the widened geometry. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

