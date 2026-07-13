---
UID: NE:wincodec.WICTiffCompressionOption
title: WICTiffCompressionOption (wincodec.h)
description: Specifies the Tagged Image File Format (TIFF) compression options.
helpviewer_keywords: ["WICTiffCompressionCCITT3","WICTiffCompressionCCITT4","WICTiffCompressionDontCare","WICTiffCompressionLZW","WICTiffCompressionLZWHDifferencing","WICTiffCompressionNone","WICTiffCompressionOption","WICTiffCompressionOption enumeration [Windows Imaging Component]","WICTiffCompressionRLE","WICTiffCompressionZIP","_wic_codec_wictiffcompressionoption","wic._wic_codec_wictiffcompressionoption","wincodec/WICTiffCompressionCCITT3","wincodec/WICTiffCompressionCCITT4","wincodec/WICTiffCompressionDontCare","wincodec/WICTiffCompressionLZW","wincodec/WICTiffCompressionLZWHDifferencing","wincodec/WICTiffCompressionNone","wincodec/WICTiffCompressionOption","wincodec/WICTiffCompressionRLE","wincodec/WICTiffCompressionZIP"]
old-location: wic\_wic_codec_wictiffcompressionoption.htm
tech.root: wic
ms.assetid: 787f6d71-6481-4236-8c3f-1b18bfb7ee88
ms.date: 12/05/2018
ms.keywords: WICTiffCompressionCCITT3, WICTiffCompressionCCITT4, WICTiffCompressionDontCare, WICTiffCompressionLZW, WICTiffCompressionLZWHDifferencing, WICTiffCompressionNone, WICTiffCompressionOption, WICTiffCompressionOption enumeration [Windows Imaging Component], WICTiffCompressionRLE, WICTiffCompressionZIP, _wic_codec_wictiffcompressionoption, wic._wic_codec_wictiffcompressionoption, wincodec/WICTiffCompressionCCITT3, wincodec/WICTiffCompressionCCITT4, wincodec/WICTiffCompressionDontCare, wincodec/WICTiffCompressionLZW, wincodec/WICTiffCompressionLZWHDifferencing, wincodec/WICTiffCompressionNone, wincodec/WICTiffCompressionOption, wincodec/WICTiffCompressionRLE, wincodec/WICTiffCompressionZIP
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICTiffCompressionOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICTiffCompressionOption
 - wincodec/WICTiffCompressionOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICTiffCompressionOption
---

# WICTiffCompressionOption enumeration


## -description

Specifies the Tagged Image File Format (TIFF) compression options.

## -enum-fields

### -field WICTiffCompressionDontCare:0

Indicates a suitable compression algorithm based on the image and pixel format.

### -field WICTiffCompressionNone:0x1

Indicates no compression.

### -field WICTiffCompressionCCITT3:0x2

Indicates a CCITT3 compression algorithm. This algorithm is only valid for 1bpp pixel formats.

### -field WICTiffCompressionCCITT4:0x3

Indicates a CCITT4 compression algorithm. This algorithm is only valid for 1bpp pixel formats.

### -field WICTiffCompressionLZW:0x4

Indicates a LZW compression algorithm.

### -field WICTiffCompressionRLE:0x5

Indicates a RLE compression algorithm. This algorithm is only valid for 1bpp pixel formats.

### -field WICTiffCompressionZIP:0x6

Indicates a ZIP compression algorithm.

### -field WICTiffCompressionLZWHDifferencing:0x7

Indicates an LZWH differencing algorithm.

### -field WICTIFFCOMPRESSIONOPTION_FORCE_DWORD:0x7fffffff

