---
UID: NS:dwrite_3.DWRITE_GLYPH_IMAGE_DATA
title: DWRITE_GLYPH_IMAGE_DATA (dwrite_3.h)
description: Data for a single glyph from GetGlyphImageData.
helpviewer_keywords: ["DWRITE_GLYPH_IMAGE_DATA","DWRITE_GLYPH_IMAGE_DATA structure [Direct Write]","directwrite.dwrite_glyph_image_data","dwrite_3/DWRITE_GLYPH_IMAGE_DATA"]
old-location: directwrite\dwrite_glyph_image_data.htm
tech.root: DirectWrite
ms.assetid: 4BBA8B7A-E2DA-445B-AE56-FFA7629E3D06
ms.date: 09/10/2025
ms.keywords: DWRITE_GLYPH_IMAGE_DATA, DWRITE_GLYPH_IMAGE_DATA structure [Direct Write], directwrite.dwrite_glyph_image_data, dwrite_3/DWRITE_GLYPH_IMAGE_DATA
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 14393
req.target-min-winversvr: Windows 10 Build 14393
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
 - DWRITE_GLYPH_IMAGE_DATA
 - dwrite_3/DWRITE_GLYPH_IMAGE_DATA
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
 - DWRITE_GLYPH_IMAGE_DATA
---

# DWRITE_GLYPH_IMAGE_DATA structure


## -description

Data for a single glyph from GetGlyphImageData.

## -struct-fields

### -field imageData

Pointer to the glyph data.

### -field imageDataSize

Size of glyph data in bytes.

### -field uniqueDataId

Unique identifier for the glyph data. Clients may use this to cache a parsed/decompressed version and tell whether a repeated call to the same font returns the same data.

### -field pixelsPerEm

Pixels per em of the returned data. For non-scalable raster data (PNG/TIFF/JPG), this can be larger or smaller than requested from GetGlyphImageData when there isn't an exact match.
          For scaling intermediate sizes, use: desired pixels per em * font em size / actual pixels per em.

### -field pixelSize

Size of image when the format is pixel data.

### -field horizontalLeftOrigin

Left origin along the horizontal Roman baseline.

### -field horizontalRightOrigin

Right origin along the horizontal Roman baseline.

### -field verticalTopOrigin

Top origin along the vertical central baseline.

### -field verticalBottomOrigin

Bottom origin along vertical central baseline.

