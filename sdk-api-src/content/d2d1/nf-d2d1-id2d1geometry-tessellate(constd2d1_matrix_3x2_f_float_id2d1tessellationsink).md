---
UID: NF:d2d1.ID2D1Geometry.Tessellate(constD2D1_MATRIX_3X2_F,FLOAT,ID2D1TessellationSink)
title: ID2D1Geometry::Tessellate (d2d1.h)
description: Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the specified tolerance. (overload 2/2)
helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","Tessellate method","ID2D1Geometry.Tessellate","ID2D1Geometry::Tessellate","ID2D1Geometry::Tessellate(const D2D1_MATRIX_3X2_F &","FLOAT","ID2D1TessellationSink)","Tessellate","Tessellate method [Direct2D]","Tessellate method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::Tessellate","direct2d.ID2D1Geometry_Tessellate_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1TessellationSink"]
old-location: direct2d\ID2D1Geometry_Tessellate_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1TessellationSink.htm
tech.root: Direct2D
ms.assetid: 0efa4d4f-ebda-49e1-9d94-dcada7374109
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Tessellate method, ID2D1Geometry.Tessellate, ID2D1Geometry::Tessellate, ID2D1Geometry::Tessellate(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1TessellationSink), Tessellate, Tessellate method [Direct2D], Tessellate method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Tessellate, direct2d.ID2D1Geometry_Tessellate_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1TessellationSink
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
 - ID2D1Geometry::Tessellate
 - d2d1/ID2D1Geometry::Tessellate
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
 - ID2D1Geometry.Tessellate
---

## -description

Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the specified tolerance.

## -parameters

### -param worldTransform

Type: [in, optional] <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to this geometry, or <b>NULL</b>.

### -param flatteningTolerance

Type: [in] <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.

### -param tessellationSink

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a>*</b>

The <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a> to which the tessellated is appended.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>

