---
UID: NF:d2d1.ID2D1Geometry.ComputeArea(constD2D1_MATRIX_3X2_F,FLOAT,FLOAT)
title: ID2D1Geometry::ComputeArea (d2d1.h)
description: Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.
helpviewer_keywords: ["ComputeArea","ComputeArea method [Direct2D]","ComputeArea method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","ComputeArea method","ID2D1Geometry.ComputeArea","ID2D1Geometry::ComputeArea","ID2D1Geometry::ComputeArea","ID2D1Geometry::ComputeArea(const D2D1_MATRIX_3X2_F","FLOAT","FLOAT)","d2d1/ID2D1Geometry::ComputeArea","direct2d.ID2D1Geometry_ComputeArea_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT"]
old-location: direct2d\ID2D1Geometry_ComputeArea_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT.htm
tech.root: Direct2D
ms.assetid: 1efc99d7-453f-4c51-a523-00c38fa00ff4
ms.date: 12/05/2018
ms.keywords: ComputeArea, ComputeArea method [Direct2D], ComputeArea method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],ComputeArea method, ID2D1Geometry.ComputeArea, ID2D1Geometry::ComputeArea, ID2D1Geometry::ComputeArea,ID2D1Geometry::ComputeArea(const D2D1_MATRIX_3X2_F,FLOAT,FLOAT), d2d1/ID2D1Geometry::ComputeArea, direct2d.ID2D1Geometry_ComputeArea_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT
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
 - ID2D1Geometry::ComputeArea
 - d2d1/ID2D1Geometry::ComputeArea
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
 - ID2D1Geometry.ComputeArea
---

## -description

Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.

## -parameters

### -param worldTransform

Type: [in, optional] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to this geometry before computing its area, or <b>NULL</b>.

### -param flatteningTolerance

Type: [in] <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.

### -param area

Type: [out] <b>FLOAT*</b>

When this this method returns, contains a pointer to the area of the transformed, flattened version of this geometry. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

