---
UID: NE:gdiplusimaging.ImageCodecFlags
title: ImageCodecFlags
author: windows-sdk-content
description: The ImageCodecFlags enumeration indicates attributes of an image codec.
old-location: gdiplus\_gdiplus_ENUM_ImageCodecFlags.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imagecodecflags.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ImageCodecFlags, ImageCodecFlags enumeration [GDI+], ImageCodecFlagsBlockingDecode, ImageCodecFlagsBuiltin, ImageCodecFlagsDecoder, ImageCodecFlagsEncoder, ImageCodecFlagsSeekableEncode, ImageCodecFlagsSupportBitmap, ImageCodecFlagsSupportVector, ImageCodecFlagsSystem, ImageCodecFlagsUser, _gdiplus_ENUM_ImageCodecFlags, gdiplus._gdiplus_ENUM_ImageCodecFlags, gdiplusimaging/ImageCodecFlags, gdiplusimaging/ImageCodecFlagsBlockingDecode, gdiplusimaging/ImageCodecFlagsBuiltin, gdiplusimaging/ImageCodecFlagsDecoder, gdiplusimaging/ImageCodecFlagsEncoder, gdiplusimaging/ImageCodecFlagsSeekableEncode, gdiplusimaging/ImageCodecFlagsSupportBitmap, gdiplusimaging/ImageCodecFlagsSupportVector, gdiplusimaging/ImageCodecFlagsSystem, gdiplusimaging/ImageCodecFlagsUser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageCodecFlags
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
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

