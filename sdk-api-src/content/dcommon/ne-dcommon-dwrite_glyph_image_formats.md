---
UID: NE:dcommon.DWRITE_GLYPH_IMAGE_FORMATS
title: DWRITE_GLYPH_IMAGE_FORMATS (dcommon.h)
description: Specifies which formats are supported in the font, either at a font-wide level or per glyph.
helpviewer_keywords: ["DWRITE_GLYPH_IMAGE_FORMATS","DWRITE_GLYPH_IMAGE_FORMATS enumeration [Direct Write]","DWRITE_GLYPH_IMAGE_FORMATS_CFF","DWRITE_GLYPH_IMAGE_FORMATS_COLR","DWRITE_GLYPH_IMAGE_FORMATS_JPEG","DWRITE_GLYPH_IMAGE_FORMATS_NONE","DWRITE_GLYPH_IMAGE_FORMATS_PNG","DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8","DWRITE_GLYPH_IMAGE_FORMATS_SVG","DWRITE_GLYPH_IMAGE_FORMATS_TIFF","DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE","dcommon/DWRITE_GLYPH_IMAGE_FORMATS","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_CFF","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_COLR","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_JPEG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_NONE","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PNG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_SVG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TIFF","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE","directwrite.dwrite_glyph_image_formats"]
old-location: directwrite\dwrite_glyph_image_formats.htm
tech.root: DirectWrite
ms.assetid: ECC868B5-3D17-4D55-8E00-AB446C1C22FE
ms.date: 12/05/2018
ms.keywords: DWRITE_GLYPH_IMAGE_FORMATS, DWRITE_GLYPH_IMAGE_FORMATS enumeration [Direct Write], DWRITE_GLYPH_IMAGE_FORMATS_CFF, DWRITE_GLYPH_IMAGE_FORMATS_COLR, DWRITE_GLYPH_IMAGE_FORMATS_JPEG, DWRITE_GLYPH_IMAGE_FORMATS_NONE, DWRITE_GLYPH_IMAGE_FORMATS_PNG, DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8, DWRITE_GLYPH_IMAGE_FORMATS_SVG, DWRITE_GLYPH_IMAGE_FORMATS_TIFF, DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE, dcommon/DWRITE_GLYPH_IMAGE_FORMATS, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_CFF, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_COLR, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_JPEG, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_NONE, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PNG, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_SVG, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TIFF, dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE, directwrite.dwrite_glyph_image_formats
req.header: dcommon.h
req.include-header: Dwrite_3.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_GLYPH_IMAGE_FORMATS
 - dcommon/DWRITE_GLYPH_IMAGE_FORMATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcommon.h
api_name:
 - DWRITE_GLYPH_IMAGE_FORMATS
---

# DWRITE_GLYPH_IMAGE_FORMATS enumeration


## -description

Specifies which formats are supported in the font, either at a font-wide level or per glyph.

## -enum-fields

### -field DWRITE_GLYPH_IMAGE_FORMATS_NONE:0x00000000

Indicates no data is available for this glyph.

### -field DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE:0x00000001

The glyph has TrueType outlines.

### -field DWRITE_GLYPH_IMAGE_FORMATS_CFF:0x00000002

The glyph has CFF outlines.

### -field DWRITE_GLYPH_IMAGE_FORMATS_COLR:0x00000004

The glyph has multilayered COLR data.

### -field DWRITE_GLYPH_IMAGE_FORMATS_SVG:0x00000008

The glyph has SVG outlines as standard XML.  Fonts may store the content gzip'd rather than plain text, indicated by the first two bytes as gzip header {0x1F 0x8B}.

### -field DWRITE_GLYPH_IMAGE_FORMATS_PNG:0x00000010

The glyph has PNG image data, with standard PNG IHDR.

### -field DWRITE_GLYPH_IMAGE_FORMATS_JPEG:0x00000020

The glyph has JPEG image data, with standard JIFF SOI header.

### -field DWRITE_GLYPH_IMAGE_FORMATS_TIFF:0x00000040

The glyph has TIFF image data.

### -field DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8:0x00000080

The glyph has raw 32-bit premultiplied BGRA data.

