---
UID: NS:d2d1_1.D2D1_DRAWING_STATE_DESCRIPTION1
title: D2D1_DRAWING_STATE_DESCRIPTION1 (d2d1_1.h)
description: Describes the drawing state of a device context.
helpviewer_keywords: ["D2D1_DRAWING_STATE_DESCRIPTION1","D2D1_DRAWING_STATE_DESCRIPTION1 structure [Direct2D]","d2d1_1/D2D1_DRAWING_STATE_DESCRIPTION1","direct2d.d2d1_drawing_state_description1"]
old-location: direct2d\d2d1_drawing_state_description1.htm
tech.root: Direct2D
ms.assetid: E1BFF353-8445-435C-8F7A-E93BFE58A794
ms.date: 12/05/2018
ms.keywords: D2D1_DRAWING_STATE_DESCRIPTION1, D2D1_DRAWING_STATE_DESCRIPTION1 structure [Direct2D], d2d1_1/D2D1_DRAWING_STATE_DESCRIPTION1, direct2d.d2d1_drawing_state_description1
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_DRAWING_STATE_DESCRIPTION1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DRAWING_STATE_DESCRIPTION1
 - d2d1_1/D2D1_DRAWING_STATE_DESCRIPTION1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2D1_1.h
api_name:
 - D2D1_DRAWING_STATE_DESCRIPTION1
---

# D2D1_DRAWING_STATE_DESCRIPTION1 structure


## -description

Describes the drawing state of a device context.

## -struct-fields

### -field antialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent nontext drawing operations.

### -field textAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations.

### -field tag1

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations.

### -field tag2

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations.

### -field transform

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to subsequent drawing operations.

### -field primitiveBlend

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_primitive_blend">D2D1_PRIMITIVE_BLEND</a></b>

The blend mode for the device context to apply to subsequent drawing operations.

### -field unitMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_unit_mode">D2D1_UNIT_MODE</a></b>

D2D1_UNIT_MODE

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-restoredrawingstate">RestoreDrawingState</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-savedrawingstate">SaveDrawingState</a>