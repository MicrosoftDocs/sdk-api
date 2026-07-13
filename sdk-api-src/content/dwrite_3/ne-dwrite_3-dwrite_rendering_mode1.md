---
UID: NE:dwrite_3.DWRITE_RENDERING_MODE1
title: DWRITE_RENDERING_MODE1 (dwrite_3.h)
description: Specifies how glyphs are rendered.
helpviewer_keywords: ["DWRITE_RENDERING_MODE1","DWRITE_RENDERING_MODE1 enumeration [Direct Write]","DWRITE_RENDERING_MODE1_ALIASED","DWRITE_RENDERING_MODE1_DEFAULT","DWRITE_RENDERING_MODE1_GDI_CLASSIC","DWRITE_RENDERING_MODE1_GDI_NATURAL","DWRITE_RENDERING_MODE1_NATURAL","DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC","DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC_DOWNSAMPLED","DWRITE_RENDERING_MODE1_OUTLINE","directwrite.dwrite_rendering_mode1","dwrite_3/DWRITE_RENDERING_MODE1","dwrite_3/DWRITE_RENDERING_MODE1_ALIASED","dwrite_3/DWRITE_RENDERING_MODE1_DEFAULT","dwrite_3/DWRITE_RENDERING_MODE1_GDI_CLASSIC","dwrite_3/DWRITE_RENDERING_MODE1_GDI_NATURAL","dwrite_3/DWRITE_RENDERING_MODE1_NATURAL","dwrite_3/DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC","dwrite_3/DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC_DOWNSAMPLED","dwrite_3/DWRITE_RENDERING_MODE1_OUTLINE"]
old-location: directwrite\dwrite_rendering_mode1.htm
tech.root: DirectWrite
ms.assetid: CAA88479-FE39-48D0-89D8-CEA0C922428A
ms.date: 09/10/2025
ms.keywords: DWRITE_RENDERING_MODE1, DWRITE_RENDERING_MODE1 enumeration [Direct Write], DWRITE_RENDERING_MODE1_ALIASED, DWRITE_RENDERING_MODE1_DEFAULT, DWRITE_RENDERING_MODE1_GDI_CLASSIC, DWRITE_RENDERING_MODE1_GDI_NATURAL, DWRITE_RENDERING_MODE1_NATURAL, DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC, DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC_DOWNSAMPLED, DWRITE_RENDERING_MODE1_OUTLINE, directwrite.dwrite_rendering_mode1, dwrite_3/DWRITE_RENDERING_MODE1, dwrite_3/DWRITE_RENDERING_MODE1_ALIASED, dwrite_3/DWRITE_RENDERING_MODE1_DEFAULT, dwrite_3/DWRITE_RENDERING_MODE1_GDI_CLASSIC, dwrite_3/DWRITE_RENDERING_MODE1_GDI_NATURAL, dwrite_3/DWRITE_RENDERING_MODE1_NATURAL, dwrite_3/DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC, dwrite_3/DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC_DOWNSAMPLED, dwrite_3/DWRITE_RENDERING_MODE1_OUTLINE
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_RENDERING_MODE1
 - dwrite_3/DWRITE_RENDERING_MODE1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_RENDERING_MODE1
---

# DWRITE_RENDERING_MODE1 enumeration


## -description

Specifies how glyphs are rendered.

## -enum-fields

### -field DWRITE_RENDERING_MODE1_DEFAULT

Specifies that the rendering mode is determined automatically, based on the font and size.

### -field DWRITE_RENDERING_MODE1_ALIASED

Specifies that no anti-aliasing is performed. Each pixel is either set to the foreground color of the text or retains the color of the background.

### -field DWRITE_RENDERING_MODE1_GDI_CLASSIC

Specifies that antialiasing is performed in the horizontal direction and the appearance of glyphs is layout-compatible with GDI using CLEARTYPE_QUALITY. 
            Use DWRITE_MEASURING_MODE_GDI_CLASSIC to get glyph advances. The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE1_GDI_NATURAL

Specifies that antialiasing is performed in the horizontal direction and the appearance of glyphs is layout-compatible with GDI using CLEARTYPE_NATURAL_QUALITY. 
          Glyph advances are close to the font design advances, but are still rounded to whole pixels. Use DWRITE_MEASURING_MODE_GDI_NATURAL to get glyph advances. 
          The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE1_NATURAL

Specifies that antialiasing is performed in the horizontal direction. This rendering mode allows glyphs to be positioned with subpixel precision and 
            is therefore suitable for natural (i.e., resolution-independent) layout. 
            The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC

Similar to natural mode except that antialiasing is performed in both the horizontal and vertical directions. 
          This is typically used at larger sizes to make curves and diagonal lines look smoother. 
          The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE1_OUTLINE

Specifies that rendering should bypass the rasterizer and use the outlines directly. This is typically used at very large sizes.

### -field DWRITE_RENDERING_MODE1_NATURAL_SYMMETRIC_DOWNSAMPLED

Similar to natural symmetric mode except that when possible, text should be rasterized in a downsampled form.

