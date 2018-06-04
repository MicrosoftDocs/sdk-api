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

# DWRITE_GLYPH_IMAGE_FORMATS enumeration


## -description


Specifies which formats are supported in the font, either at a font-wide level or per glyph.


## -enum-fields




### -field DWRITE_GLYPH_IMAGE_FORMATS_NONE

Indicates no data is available for this glyph.


### -field DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE

The glyph has TrueType outlines.


### -field DWRITE_GLYPH_IMAGE_FORMATS_CFF

The glyph has CFF outlines.


### -field DWRITE_GLYPH_IMAGE_FORMATS_COLR

The glyph has multilayered COLR data.


### -field DWRITE_GLYPH_IMAGE_FORMATS_SVG

The glyph has SVG outlines as standard XML.  Fonts may store the content gzip'd rather than plain text, indicated by the first two bytes as gzip header {0x1F 0x8B}.


### -field DWRITE_GLYPH_IMAGE_FORMATS_PNG

The glyph has PNG image data, with standard PNG IHDR.


### -field DWRITE_GLYPH_IMAGE_FORMATS_JPEG

The glyph has JPEG image data, with standard JIFF SOI header.


### -field DWRITE_GLYPH_IMAGE_FORMATS_TIFF

The glyph has TIFF image data.


### -field DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8

The glyph has raw 32-bit premultiplied BGRA data.

