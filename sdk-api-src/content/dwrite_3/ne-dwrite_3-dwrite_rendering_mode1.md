---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

