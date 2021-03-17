---
UID: NF:d2d1helper.DrawingStateDescription
title: DrawingStateDescription function (d2d1helper.h)
description: Creates a D2D1_DRAWING_STATE_DESCRIPTION structure.
helpviewer_keywords: ["DrawingStateDescription","DrawingStateDescription function [Direct2D]","d2d1helper/DrawingStateDescription","direct2d.drawingstatedescription"]
old-location: direct2d\drawingstatedescription.htm
tech.root: Direct2D
ms.assetid: a1f81523-bf9b-4807-a095-d2f4081698e3
ms.date: 12/05/2018
ms.keywords: DrawingStateDescription, DrawingStateDescription function [Direct2D], d2d1helper/DrawingStateDescription, direct2d.drawingstatedescription
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
 - DrawingStateDescription
 - d2d1helper/DrawingStateDescription
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
 - DrawingStateDescription
---

# DrawingStateDescription function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description">D2D1_DRAWING_STATE_DESCRIPTION</a> structure.

## -parameters

### -param antialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent non-text drawing operations. The default value is  <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE_PER_PRIMITIVE</a>.

### -param textAntialiasMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE</a></b>

The antialiasing mode for subsequent text and glyph drawing operations. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE_DEFAULT</a>.

### -param tag1

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations. The default value is 0.

### -param tag2

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a></b>

A label for subsequent drawing operations. The default value is 0.

### -param transform [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transformation to be applied to subsequent drawing operations.  The default value is provided by the <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix"> D2D1::IdentityMatrix</a> function, which returns the identity matrix.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description">D2D1_DRAWING_STATE_DESCRIPTION</a></b>

A structure that describes the drawing state of a render target.