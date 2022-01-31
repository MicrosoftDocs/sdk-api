---
UID: NE:d2d1effects.D2D1_COLORMATRIX_PROP
title: D2D1_COLORMATRIX_PROP (d2d1effects.h)
description: Identifiers for the properties of the Color matrix effect.
helpviewer_keywords: ["D2D1_COLORMATRIX_PROP","D2D1_COLORMATRIX_PROP enumeration [Direct2D]","D2D1_COLORMATRIX_PROP_ALPHA_MODE","D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT","D2D1_COLORMATRIX_PROP_COLOR_MATRIX","d2d1effects/D2D1_COLORMATRIX_PROP","d2d1effects/D2D1_COLORMATRIX_PROP_ALPHA_MODE","d2d1effects/D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT","d2d1effects/D2D1_COLORMATRIX_PROP_COLOR_MATRIX","direct2d.d2d1_colormatrix_prop"]
old-location: direct2d\d2d1_colormatrix_prop.htm
tech.root: Direct2D
ms.assetid: 7A171DAF-08E4-46FF-9FAF-54A83E805555
ms.date: 12/05/2018
ms.keywords: D2D1_COLORMATRIX_PROP, D2D1_COLORMATRIX_PROP enumeration [Direct2D], D2D1_COLORMATRIX_PROP_ALPHA_MODE, D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT, D2D1_COLORMATRIX_PROP_COLOR_MATRIX, d2d1effects/D2D1_COLORMATRIX_PROP, d2d1effects/D2D1_COLORMATRIX_PROP_ALPHA_MODE, d2d1effects/D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_COLORMATRIX_PROP_COLOR_MATRIX, direct2d.d2d1_colormatrix_prop
req.header: d2d1effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: D2D1_COLORMATRIX_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COLORMATRIX_PROP
 - d2d1effects/D2D1_COLORMATRIX_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_COLORMATRIX_PROP
---

# D2D1_COLORMATRIX_PROP enumeration


## -description

Identifiers for the properties of the <a href="/windows/desktop/Direct2D/color-matrix">Color matrix effect</a>.

## -enum-fields

### -field D2D1_COLORMATRIX_PROP_COLOR_MATRIX:0

A 5x4 matrix of float values. The elements in the matrix are not bounded and are unitless.
          

The type is <a href="/windows/desktop/Direct2D/d2d1-matrix-5x4-f">D2D1_MATRIX_5X4_F</a>.

The default value is the identity matrix, Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).

### -field D2D1_COLORMATRIX_PROP_ALPHA_MODE:1

The alpha mode of the output. 
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_colormatrix_alpha_mode">D2D1_COLORMATRIX_ALPHA_MODE</a>.

The default value is D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED.

### -field D2D1_COLORMATRIX_PROP_CLAMP_OUTPUT:2

Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph. 
          The effect clamps the values before it premultiplies the alpha.
          

If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
          but other effects and the output surface may clamp the values if they are not of high enough precision.

The type is BOOL.

The default value is FALSE.

### -field D2D1_COLORMATRIX_PROP_FORCE_DWORD:0xffffffff
