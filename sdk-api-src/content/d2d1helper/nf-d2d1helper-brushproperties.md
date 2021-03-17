---
UID: NF:d2d1helper.BrushProperties
title: BrushProperties function (d2d1helper.h)
description: Creates a D2D1_BRUSH_PROPERTIES structure.
helpviewer_keywords: ["BrushProperties","BrushProperties function [Direct2D]","d2d1helper/BrushProperties","direct2d.brushproperties"]
old-location: direct2d\brushproperties.htm
tech.root: Direct2D
ms.assetid: eeb438e4-300a-4d7d-b8bf-91baba4a729e
ms.date: 12/05/2018
ms.keywords: BrushProperties, BrushProperties function [Direct2D], d2d1helper/BrushProperties, direct2d.brushproperties
req.header: d2d1helper.h
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
 - BrushProperties
 - d2d1helper/BrushProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - BrushProperties
---

# BrushProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a> structure.

## -parameters

### -param opacity [in]

Type: <b>FLOAT</b>

The base opacity of the brush. The default value is 1.0.

### -param transform [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to the brush. The default value is <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix">D2D1::IdentityMatrix</a>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a></b>

The new brush properties structure.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>