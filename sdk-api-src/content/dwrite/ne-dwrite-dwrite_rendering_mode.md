---
UID: NE:dwrite.DWRITE_RENDERING_MODE
title: DWRITE_RENDERING_MODE (dwrite.h)
description: Represents a method of rendering glyphs.
helpviewer_keywords: ["DWRITE_RENDERING_MODE","DWRITE_RENDERING_MODE (Windows 8 and later)","DWRITE_RENDERING_MODE enumeration [Direct Write]","DWRITE_RENDERING_MODE_ALIASED","DWRITE_RENDERING_MODE_DEFAULT","DWRITE_RENDERING_MODE_GDI_CLASSIC","DWRITE_RENDERING_MODE_GDI_NATURAL","DWRITE_RENDERING_MODE_NATURAL","DWRITE_RENDERING_MODE_NATURAL_SYMMETRIC","DWRITE_RENDERING_MODE_OUTLINE","directwrite.dwrite_rendering_mode","dwrite/DWRITE_RENDERING_MODE","dwrite/DWRITE_RENDERING_MODE_ALIASED","dwrite/DWRITE_RENDERING_MODE_DEFAULT","dwrite/DWRITE_RENDERING_MODE_GDI_CLASSIC","dwrite/DWRITE_RENDERING_MODE_GDI_NATURAL","dwrite/DWRITE_RENDERING_MODE_NATURAL","dwrite/DWRITE_RENDERING_MODE_NATURAL_SYMMETRIC","dwrite/DWRITE_RENDERING_MODE_OUTLINE"]
old-location: directwrite\dwrite_rendering_mode.htm
tech.root: DirectWrite
ms.assetid: c6b2c15a-be22-49ce-affd-1369e23f4d6b
ms.date: 12/05/2018
ms.keywords: DWRITE_RENDERING_MODE, DWRITE_RENDERING_MODE (Windows 8 and later) , DWRITE_RENDERING_MODE enumeration [Direct Write], DWRITE_RENDERING_MODE_ALIASED, DWRITE_RENDERING_MODE_DEFAULT, DWRITE_RENDERING_MODE_GDI_CLASSIC, DWRITE_RENDERING_MODE_GDI_NATURAL, DWRITE_RENDERING_MODE_NATURAL, DWRITE_RENDERING_MODE_NATURAL_SYMMETRIC, DWRITE_RENDERING_MODE_OUTLINE, directwrite.dwrite_rendering_mode, dwrite/DWRITE_RENDERING_MODE, dwrite/DWRITE_RENDERING_MODE_ALIASED, dwrite/DWRITE_RENDERING_MODE_DEFAULT, dwrite/DWRITE_RENDERING_MODE_GDI_CLASSIC, dwrite/DWRITE_RENDERING_MODE_GDI_NATURAL, dwrite/DWRITE_RENDERING_MODE_NATURAL, dwrite/DWRITE_RENDERING_MODE_NATURAL_SYMMETRIC, dwrite/DWRITE_RENDERING_MODE_OUTLINE
req.header: dwrite.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_RENDERING_MODE
 - dwrite/DWRITE_RENDERING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_RENDERING_MODE
---

# DWRITE_RENDERING_MODE enumeration


## -description

Represents a method of rendering glyphs.
      
<div class="alert"><b>Note</b>  This topic is about <b>DWRITE_RENDERING_MODE</b> in Windows 8 and later.  For info on the previous version see the Remarks section. </div><div> </div>

## -enum-fields

### -field DWRITE_RENDERING_MODE_DEFAULT

Specifies that the rendering mode is determined automatically, based on the font and size.

### -field DWRITE_RENDERING_MODE_ALIASED

Specifies that no anti-aliasing is performed. Each pixel is either set to the foreground color of the text or retains the color of the background.

### -field DWRITE_RENDERING_MODE_GDI_CLASSIC

Specifies that antialiasing is performed in the horizontal direction and the appearance of glyphs is layout-compatible with GDI using CLEARTYPE_QUALITY.
            Use DWRITE_MEASURING_MODE_GDI_CLASSIC to get glyph advances. The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE_GDI_NATURAL

Specifies that antialiasing is performed in the horizontal direction and the appearance of glyphs is layout-compatible with GDI using CLEARTYPE_NATURAL_QUALITY.
          Glyph advances are close to the font design advances, but are still rounded to whole pixels. Use DWRITE_MEASURING_MODE_GDI_NATURAL to get glyph advances. 
          The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE_NATURAL

Specifies that antialiasing is performed in the horizontal direction. This rendering mode allows glyphs to be positioned with subpixel precision and 
            is therefore suitable
            for natural (i.e., resolution-independent) layout. The antialiasing may be either ClearType or grayscale depending on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE_NATURAL_SYMMETRIC

Similar to natural mode except that antialiasing is performed in both the horizontal and vertical directions. 
          This is typically used at larger sizes to make curves and diagonal lines look smoother. The antialiasing may be either ClearType or grayscale depending 
          on the text antialiasing mode.

### -field DWRITE_RENDERING_MODE_OUTLINE

Specifies that rendering should bypass the rasterizer and use the outlines directly. This is typically used at very large sizes.

### -field DWRITE_RENDERING_MODE_CLEARTYPE_GDI_CLASSIC

### -field DWRITE_RENDERING_MODE_CLEARTYPE_GDI_NATURAL

### -field DWRITE_RENDERING_MODE_CLEARTYPE_NATURAL

### -field DWRITE_RENDERING_MODE_CLEARTYPE_NATURAL_SYMMETRIC

## -remarks

<h3><a id="DWRITE_RENDERING_MODE_previous_to_Windows_8"></a><a id="dwrite_rendering_mode_previous_to_windows_8"></a><a id="DWRITE_RENDERING_MODE_PREVIOUS_TO_WINDOWS_8"></a>DWRITE_RENDERING_MODE previous to Windows 8</h3>

<pre class="syntax">enum DWRITE_RENDERING_MODE {
  DWRITE_RENDERING_MODE_DEFAULT, 
  DWRITE_RENDERING_MODE_ALIASED, 
  DWRITE_RENDERING_MODE_CLEARTYPE_GDI_CLASSIC, 
  DWRITE_RENDERING_MODE_CLEARTYPE_GDI_NATURAL, 
  DWRITE_RENDERING_MODE_CLEARTYPE_NATURAL, 
  DWRITE_RENDERING_MODE_CLEARTYPE_NATURAL_SYMMETRIC, 
  DWRITE_RENDERING_MODE_OUTLINE 

};</pre>

