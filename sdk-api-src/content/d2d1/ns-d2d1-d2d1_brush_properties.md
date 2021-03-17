---
UID: NS:d2d1.D2D1_BRUSH_PROPERTIES
title: D2D1_BRUSH_PROPERTIES (d2d1.h)
description: Describes the opacity and transformation of a brush.
helpviewer_keywords: ["D2D1_BRUSH_PROPERTIES","D2D1_BRUSH_PROPERTIES structure [Direct2D]","d2d1/D2D1_BRUSH_PROPERTIES","direct2d.D2D1_BRUSH_PROPERTIES"]
old-location: direct2d\D2D1_BRUSH_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 37b2fc18-a320-41c0-8717-dcd561a2f2df
ms.date: 12/05/2018
ms.keywords: D2D1_BRUSH_PROPERTIES, D2D1_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_BRUSH_PROPERTIES, direct2d.D2D1_BRUSH_PROPERTIES
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BRUSH_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BRUSH_PROPERTIES
 - d2d1/D2D1_BRUSH_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BRUSH_PROPERTIES
---

# D2D1_BRUSH_PROPERTIES structure


## -description

Describes the opacity and transformation of a brush.

## -struct-fields

### -field opacity

Type: <b>FLOAT</b>

A value between 0.0f and 1.0f, inclusive, that specifies the degree of opacity of the brush.

### -field transform

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation that is applied to the brush.

## -remarks

This structure is used when creating a brush. For convenience, Direct2D provides the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-brushproperties">D2D1::BrushProperties</a> function for creating <b>D2D1_BRUSH_PROPERTIES</b> structures.


After creating a brush, you can change its opacity or transform by calling the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1brush-setopacity">SetOpacity</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)">SetTransform</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1helper/nf-d2d1helper-brushproperties">D2D1::BrushProperties</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1brush-setopacity">SetOpacity</a>

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)">SetTransform</a>

