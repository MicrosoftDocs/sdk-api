---
UID: NE:gdiplusimaging.ImageCodecFlags
title: ImageCodecFlags (gdiplusimaging.h)
description: The ImageCodecFlags enumeration indicates attributes of an image codec.
helpviewer_keywords: ["ImageCodecFlags","ImageCodecFlags enumeration [GDI+]","ImageCodecFlagsBlockingDecode","ImageCodecFlagsBuiltin","ImageCodecFlagsDecoder","ImageCodecFlagsEncoder","ImageCodecFlagsSeekableEncode","ImageCodecFlagsSupportBitmap","ImageCodecFlagsSupportVector","ImageCodecFlagsSystem","ImageCodecFlagsUser","_gdiplus_ENUM_ImageCodecFlags","gdiplus._gdiplus_ENUM_ImageCodecFlags","gdiplusimaging/ImageCodecFlags","gdiplusimaging/ImageCodecFlagsBlockingDecode","gdiplusimaging/ImageCodecFlagsBuiltin","gdiplusimaging/ImageCodecFlagsDecoder","gdiplusimaging/ImageCodecFlagsEncoder","gdiplusimaging/ImageCodecFlagsSeekableEncode","gdiplusimaging/ImageCodecFlagsSupportBitmap","gdiplusimaging/ImageCodecFlagsSupportVector","gdiplusimaging/ImageCodecFlagsSystem","gdiplusimaging/ImageCodecFlagsUser"]
old-location: gdiplus\_gdiplus_ENUM_ImageCodecFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imagecodecflags.htm
ms.date: 12/05/2018
ms.keywords: ImageCodecFlags, ImageCodecFlags enumeration [GDI+], ImageCodecFlagsBlockingDecode, ImageCodecFlagsBuiltin, ImageCodecFlagsDecoder, ImageCodecFlagsEncoder, ImageCodecFlagsSeekableEncode, ImageCodecFlagsSupportBitmap, ImageCodecFlagsSupportVector, ImageCodecFlagsSystem, ImageCodecFlagsUser, _gdiplus_ENUM_ImageCodecFlags, gdiplus._gdiplus_ENUM_ImageCodecFlags, gdiplusimaging/ImageCodecFlags, gdiplusimaging/ImageCodecFlagsBlockingDecode, gdiplusimaging/ImageCodecFlagsBuiltin, gdiplusimaging/ImageCodecFlagsDecoder, gdiplusimaging/ImageCodecFlagsEncoder, gdiplusimaging/ImageCodecFlagsSeekableEncode, gdiplusimaging/ImageCodecFlagsSupportBitmap, gdiplusimaging/ImageCodecFlagsSupportVector, gdiplusimaging/ImageCodecFlagsSystem, gdiplusimaging/ImageCodecFlagsUser
req.header: gdiplusimaging.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ImageCodecFlags
 - gdiplusimaging/ImageCodecFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageCodecFlags
---

# ImageCodecFlags enumeration


## -description

The <b>ImageCodecFlags</b> enumeration indicates attributes of an image codec.

## -enum-fields

### -field ImageCodecFlagsEncoder:0x00000001

Indicates that the codec supports encoding (saving).

### -field ImageCodecFlagsDecoder:0x00000002

Indicates that the codec supports decoding (reading).

### -field ImageCodecFlagsSupportBitmap:0x00000004

Indicates that the codec supports raster images (bitmaps).

### -field ImageCodecFlagsSupportVector:0x00000008

Indicates that the codec supports vector images (metafiles).

### -field ImageCodecFlagsSeekableEncode:0x00000010

Indicates that an encoder requires a seekable output stream.

### -field ImageCodecFlagsBlockingDecode:0x00000020

Indicates that a decoder has blocking behavior during the decoding process.

### -field ImageCodecFlagsBuiltin:0x00010000

Indicates that the codec is built in to GDI+.

### -field ImageCodecFlagsSystem:0x00020000

Not used in GDI+ version 1.0.

### -field ImageCodecFlagsUser:0x00040000

Not used in GDI+ version 1.0.

