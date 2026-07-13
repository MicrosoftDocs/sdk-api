---
UID: NE:dcommon.DWRITE_GLYPH_IMAGE_FORMATS
title: DWRITE_GLYPH_IMAGE_FORMATS (dcommon.h)
description: Specifies which formats are supported in the font, either at a font-wide level or per glyph.
helpviewer_keywords: ["DWRITE_GLYPH_IMAGE_FORMATS","DWRITE_GLYPH_IMAGE_FORMATS enumeration [Direct Write]","DWRITE_GLYPH_IMAGE_FORMATS_CFF","DWRITE_GLYPH_IMAGE_FORMATS_COLR","DWRITE_GLYPH_IMAGE_FORMATS_JPEG","DWRITE_GLYPH_IMAGE_FORMATS_NONE","DWRITE_GLYPH_IMAGE_FORMATS_PNG","DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8","DWRITE_GLYPH_IMAGE_FORMATS_SVG","DWRITE_GLYPH_IMAGE_FORMATS_TIFF","DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE","dcommon/DWRITE_GLYPH_IMAGE_FORMATS","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_CFF","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_COLR","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_JPEG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_NONE","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PNG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_SVG","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TIFF","dcommon/DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE","directwrite.dwrite_glyph_image_formats"]
old-location: directwrite\dwrite_glyph_image_formats.htm
tech.root: DirectWrite
ms.assetid: ECC868B5-3D17-4D55-8E00-AB446C1C22FE
ms.date: 09/06/2023
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

## -description

> [!NOTE]
> **Some information relates to pre-released product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.**

Defines constants that specify which formats are supported in a font, either at a font-wide level or per glyph.

For color fonts, these formats can be used to represent color glyphs. Fonts can contain multiple drawable data formats for glyphs. And an app can use these values to tell DirectWrite which formats to return when splitting a color glyph run.

## -enum-fields

### -field DWRITE_GLYPH_IMAGE_FORMATS_NONE:0x00000000

Specifies that no data is available for this glyph.

### -field DWRITE_GLYPH_IMAGE_FORMATS_TRUETYPE:0x00000001

Specifies that the glyph has TrueType outlines.

### -field DWRITE_GLYPH_IMAGE_FORMATS_CFF:0x00000002

Specifies that the glyph has CFF outlines.

### -field DWRITE_GLYPH_IMAGE_FORMATS_COLR:0x00000004

Specifies that the glyph has multilayered COLR data.

### -field DWRITE_GLYPH_IMAGE_FORMATS_SVG:0x00000008

Specifies that the glyph has SVG outlines as standard XML. Fonts may store the content gzip'd rather than plain text, indicated by the first two bytes as gzip header {0x1F 0x8B}.

### -field DWRITE_GLYPH_IMAGE_FORMATS_PNG:0x00000010

Specifies that the glyph has PNG image data, with standard PNG IHDR.

### -field DWRITE_GLYPH_IMAGE_FORMATS_JPEG:0x00000020

Specifies that the glyph has JPEG image data, with standard JIFF SOI header.

### -field DWRITE_GLYPH_IMAGE_FORMATS_TIFF:0x00000040

Specifies that the glyph has TIFF image data.

### -field DWRITE_GLYPH_IMAGE_FORMATS_PREMULTIPLIED_B8G8R8A8:0x00000080

Specifies that the glyph has raw 32-bit premultiplied BGRA data.

### -field DWRITE_GLYPH_IMAGE_FORMATS_COLR_PAINT_TREE:0x00000100

> [!IMPORTANT]
> The **DWRITE_GLYPH_IMAGE_FORMATS_COLR_PAINT_TREE** constant is available in pre-release versions of the [Windows Insider Preview](https://www.microsoft.com/software-download/windowsinsiderpreviewSDK).

Specifies that the glyph is represented by a tree of paint elements in the font's COLR table.
