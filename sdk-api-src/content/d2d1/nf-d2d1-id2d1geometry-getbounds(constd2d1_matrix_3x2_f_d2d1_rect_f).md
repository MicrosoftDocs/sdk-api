---
UID: NF:d2d1.ID2D1Geometry.GetBounds(constD2D1_MATRIX_3X2_F,D2D1_RECT_F)
title: ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F) (d2d1.h)
description: Retrieves the bounds of the geometry. (overload 1/2)
helpviewer_keywords: ["GetBounds","GetBounds method [Direct2D]","GetBounds method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","GetBounds method","ID2D1Geometry.GetBounds","ID2D1Geometry.GetBounds(const D2D1_MATRIX_3X2_F","D2D1_RECT_F)","ID2D1Geometry::GetBounds","ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F","D2D1_RECT_F)","d2d1/ID2D1Geometry::GetBounds","direct2d.ID2D1Geometry_GetBounds_ptr_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F"]
old-location: direct2d\ID2D1Geometry_GetBounds_ptr_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F.htm
tech.root: Direct2D
ms.assetid: 5dc79a72-60d5-4a6d-94e6-d8a476d01c19
ms.date: 12/05/2018
ms.keywords: GetBounds, GetBounds method [Direct2D], GetBounds method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],GetBounds method, ID2D1Geometry.GetBounds, ID2D1Geometry.GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F), ID2D1Geometry::GetBounds, ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F), d2d1/ID2D1Geometry::GetBounds, direct2d.ID2D1Geometry_GetBounds_ptr_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F
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
 - ID2D1Geometry::GetBounds
 - d2d1/ID2D1Geometry::GetBounds
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
 - ID2D1Geometry.GetBounds
---

# ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F)


## -description

Retrieves the bounds of the geometry.

## -parameters

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to this geometry before calculating its bounds, or <b>NULL</b>.

### -param bounds [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

When this method returns, contains the bounds of this geometry. If the bounds are empty, this parameter will be a rect where <i>bounds.left</i> &gt; <i>bounds.right</i>. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

