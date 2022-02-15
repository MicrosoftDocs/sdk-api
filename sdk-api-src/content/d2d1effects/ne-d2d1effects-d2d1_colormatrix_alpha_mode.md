---
UID: NE:d2d1effects.D2D1_COLORMATRIX_ALPHA_MODE
title: D2D1_COLORMATRIX_ALPHA_MODE (d2d1effects.h)
description: The alpha mode of the output of the Color matrix effect.
helpviewer_keywords: ["D2D1_COLORMATRIX_ALPHA_MODE","D2D1_COLORMATRIX_ALPHA_MODE enumeration [Direct2D]","D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED","D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT","d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE","d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED","d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT","direct2d.d2d1_colormatrix_alpha_mode"]
old-location: direct2d\d2d1_colormatrix_alpha_mode.htm
tech.root: Direct2D
ms.assetid: 7D7CB142-5758-4745-A4CD-41B3E2465562
ms.date: 12/05/2018
ms.keywords: D2D1_COLORMATRIX_ALPHA_MODE, D2D1_COLORMATRIX_ALPHA_MODE enumeration [Direct2D], D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED, D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT, d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE, d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED, d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT, direct2d.d2d1_colormatrix_alpha_mode
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
req.typenames: D2D1_COLORMATRIX_ALPHA_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COLORMATRIX_ALPHA_MODE
 - d2d1effects/D2D1_COLORMATRIX_ALPHA_MODE
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
 - D2D1_COLORMATRIX_ALPHA_MODE
---

# D2D1_COLORMATRIX_ALPHA_MODE enumeration


## -description

The alpha mode of the output of the <a href="/windows/desktop/Direct2D/color-matrix">Color matrix effect</a>.

## -enum-fields

### -field D2D1_COLORMATRIX_ALPHA_MODE_PREMULTIPLIED:1

The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.

### -field D2D1_COLORMATRIX_ALPHA_MODE_STRAIGHT:2

The effect applies the color matrix directly to the input, and doesn't premultiply the output.

### -field D2D1_COLORMATRIX_ALPHA_MODE_FORCE_DWORD:0xffffffff
