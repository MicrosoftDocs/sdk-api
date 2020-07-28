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
f1_keywords:
- gdiplusimaging/ImageCodecFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Gdiplusimaging.h
api_name:
- ImageCodecFlags
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageCodecFlags enumeration


## -description


The <b>ImageCodecFlags</b> enumeration indicates attributes of an image codec.


## -enum-fields




### -field ImageCodecFlagsEncoder

Indicates that the codec supports encoding (saving). 


### -field ImageCodecFlagsDecoder

Indicates that the codec supports decoding (reading). 


### -field ImageCodecFlagsSupportBitmap

Indicates that the codec supports raster images (bitmaps). 


### -field ImageCodecFlagsSupportVector

Indicates that the codec supports vector images (metafiles). 


### -field ImageCodecFlagsSeekableEncode

Indicates that an encoder requires a seekable output stream. 


### -field ImageCodecFlagsBlockingDecode

Indicates that a decoder has blocking behavior during the decoding process. 


### -field ImageCodecFlagsBuiltin

Indicates that the codec is built in to GDI+. 


### -field ImageCodecFlagsSystem

Not used in GDI+ version 1.0. 


### -field ImageCodecFlagsUser

Not used in GDI+ version 1.0. 

