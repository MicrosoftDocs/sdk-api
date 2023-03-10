---
UID: NF:d2d1.ID2D1Geometry.ComputeLength(constD2D1_MATRIX_3X2_F&,FLOAT)
title: ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT) (d2d1.h)
description: Calculates the length of the geometry as though each segment were unrolled into a line. (overload 1/4)
helpviewer_keywords: ["ComputeLength","ComputeLength method [Direct2D]","ComputeLength method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","ComputeLength method","ID2D1Geometry.ComputeLength","ID2D1Geometry.ComputeLength(const D2D1_MATRIX_3X2_F &","FLOAT)","ID2D1Geometry::ComputeLength","ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &","FLOAT)","ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F","FLOAT","FLOAT)","d2d1/ID2D1Geometry::ComputeLength","direct2d.ID2D1Geometry_ComputeLength_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT"]
old-location: direct2d\ID2D1Geometry_ComputeLength_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT.htm
tech.root: Direct2D
ms.assetid: 8f91ceca-c862-4173-b819-2a2668845c29
ms.date: 12/05/2018
ms.keywords: ComputeLength, ComputeLength method [Direct2D], ComputeLength method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],ComputeLength method, ID2D1Geometry.ComputeLength, ID2D1Geometry.ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT), ID2D1Geometry::ComputeLength, ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F &,FLOAT), ID2D1Geometry::ComputeLength(const D2D1_MATRIX_3X2_F,FLOAT,FLOAT), d2d1/ID2D1Geometry::ComputeLength, direct2d.ID2D1Geometry_ComputeLength_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_FLOAT
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
 - ID2D1Geometry::ComputeLength
 - d2d1/ID2D1Geometry::ComputeLength
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
 - ID2D1Geometry.ComputeLength
---

## -description

Calculates the length of the geometry as though each segment were unrolled into a line.

## -parameters

### -param worldTransform

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a> &</b>

The transform to apply to the geometry before calculating its length.

### -param length

Type: [out] <b>FLOAT*</b>

When this method returns, contains a pointer to the length of the geometry. For closed geometries, the length includes an implicit closing segment. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

