---
UID: NS:d2d1.D2D1_DRAWING_STATE_DESCRIPTION
title: D2D1_DRAWING_STATE_DESCRIPTION (d2d1.h)
description: Describes the drawing state of a render target.
helpviewer_keywords: ["D2D1_DRAWING_STATE_DESCRIPTION","D2D1_DRAWING_STATE_DESCRIPTION structure [Direct2D]","d2d1/D2D1_DRAWING_STATE_DESCRIPTION","direct2d.D2D1_DRAWING_STATE_DESCRIPTION"]
old-location: direct2d\D2D1_DRAWING_STATE_DESCRIPTION.htm
tech.root: Direct2D
ms.assetid: ba4adc4b-4d86-40c4-8911-1c800d3c6f3e
ms.date: 12/05/2018
ms.keywords: D2D1_DRAWING_STATE_DESCRIPTION, D2D1_DRAWING_STATE_DESCRIPTION structure [Direct2D], d2d1/D2D1_DRAWING_STATE_DESCRIPTION, direct2d.D2D1_DRAWING_STATE_DESCRIPTION
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
req.typenames: D2D1_DRAWING_STATE_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DRAWING_STATE_DESCRIPTION
 - d2d1/D2D1_DRAWING_STATE_DESCRIPTION
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
 - D2D1_DRAWING_STATE_DESCRIPTION
---

# D2D1_DRAWING_STATE_DESCRIPTION structure


## -description

Describes the drawing state of a render target.

## -struct-fields

### -field antialiasMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent nontext drawing operations.

### -field textAntialiasMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations.

### -field tag1

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations.

### -field tag2

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations.

### -field transform

Type: <b><a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation to apply to subsequent drawing operations.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-restoredrawingstate">RestoreDrawingState</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-savedrawingstate">SaveDrawingState</a>

