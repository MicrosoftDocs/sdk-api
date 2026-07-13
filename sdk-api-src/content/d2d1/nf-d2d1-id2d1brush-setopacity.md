---
UID: NF:d2d1.ID2D1Brush.SetOpacity
title: ID2D1Brush::SetOpacity (d2d1.h)
description: Sets the degree of opacity of this brush.
helpviewer_keywords: ["ID2D1Brush interface [Direct2D]","SetOpacity method","ID2D1Brush.SetOpacity","ID2D1Brush::SetOpacity","SetOpacity","SetOpacity method [Direct2D]","SetOpacity method [Direct2D]","ID2D1Brush interface","d2d1/ID2D1Brush::SetOpacity","direct2d.ID2D1Brush_SetOpacity"]
old-location: direct2d\ID2D1Brush_SetOpacity.htm
tech.root: Direct2D
ms.assetid: c2e6df27-4007-4f2e-9567-439dd3842318
ms.date: 12/05/2018
ms.keywords: ID2D1Brush interface [Direct2D],SetOpacity method, ID2D1Brush.SetOpacity, ID2D1Brush::SetOpacity, SetOpacity, SetOpacity method [Direct2D], SetOpacity method [Direct2D],ID2D1Brush interface, d2d1/ID2D1Brush::SetOpacity, direct2d.ID2D1Brush_SetOpacity
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
 - ID2D1Brush::SetOpacity
 - d2d1/ID2D1Brush::SetOpacity
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
 - ID2D1Brush.SetOpacity
---

# ID2D1Brush::SetOpacity


## -description

Sets the degree of opacity of this brush.

## -parameters

### -param opacity

Type: <b>FLOAT</b>

A value between zero and 1 that indicates the opacity of the brush. This value is a constant multiplier that linearly scales the alpha value of all pixels filled by the brush. The opacity values are clamped in the range 0–1 before they are multiplied together.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>

