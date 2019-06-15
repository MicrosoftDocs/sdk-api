---
UID: NF:d2d1.ID2D1Geometry.Tessellate(const D2D1_MATRIX_3X2_F,ID2D1TessellationSink)
title: ID2D1Geometry::Tessellate(const D2D1_MATRIX_3X2_F,ID2D1TessellationSink) (d2d1.h)
author: windows-sdk-content
description: Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the default tolerance.
old-location: direct2d\ID2D1Geometry_Tessellate_ref_D2D_MATRIX_3X2_F_ptr_ID2D1TessellationSink.htm
tech.root: Direct2D
ms.assetid: 7d2762d3-1151-48b1-b0fd-507e0993717c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Tessellate method, ID2D1Geometry.Tessellate, ID2D1Geometry.Tessellate(const D2D1_MATRIX_3X2_F,ID2D1TessellationSink), ID2D1Geometry::Tessellate, ID2D1Geometry::Tessellate(const D2D1_MATRIX_3X2_F,ID2D1TessellationSink), Tessellate, Tessellate method [Direct2D], Tessellate method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Tessellate, direct2d.ID2D1Geometry_Tessellate_ref_D2D_MATRIX_3X2_F_ptr_ID2D1TessellationSink
ms.topic: method
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
 - ID2D1Geometry.Tessellate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry::Tessellate(const D2D1_MATRIX_3X2_F,ID2D1TessellationSink)


## -description


Creates a set of clockwise-wound triangles that cover the geometry after it has been transformed using the specified matrix and flattened using the default tolerance.


## -parameters




### -param worldTransform [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transform to apply to this geometry.


### -param tessellationSink [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a> to which the tessellated is appended.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

