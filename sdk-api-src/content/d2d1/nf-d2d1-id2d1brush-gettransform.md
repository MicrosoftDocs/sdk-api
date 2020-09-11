---
UID: NF:d2d1.ID2D1Brush.GetTransform
title: ID2D1Brush::GetTransform (d2d1.h)
description: Gets the transform applied to this brush.
helpviewer_keywords: ["GetTransform","GetTransform method [Direct2D]","GetTransform method [Direct2D]","ID2D1Brush interface","ID2D1Brush interface [Direct2D]","GetTransform method","ID2D1Brush.GetTransform","ID2D1Brush::GetTransform","d2d1/ID2D1Brush::GetTransform","direct2d.ID2D1Brush_GetTransform"]
old-location: direct2d\ID2D1Brush_GetTransform.htm
tech.root: Direct2D
ms.assetid: f28282e8-f994-4501-a327-fcceb8379f70
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [Direct2D], GetTransform method [Direct2D],ID2D1Brush interface, ID2D1Brush interface [Direct2D],GetTransform method, ID2D1Brush.GetTransform, ID2D1Brush::GetTransform, d2d1/ID2D1Brush::GetTransform, direct2d.ID2D1Brush_GetTransform
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
 - ID2D1Brush::GetTransform
 - d2d1/ID2D1Brush::GetTransform
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
 - ID2D1Brush.GetTransform
---

# ID2D1Brush::GetTransform


## -description

Gets the transform applied to this brush.

## -parameters

### -param transform [out]

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform applied to this brush.

## -remarks

When the brush transform is the identity matrix, the brush appears in the same coordinate space as the render target in which it is drawn.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>

