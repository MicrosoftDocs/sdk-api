---
UID: NE:wincodec.WICComponentType
title: WICComponentType (wincodec.h)
description: Specifies the type of Windows Imaging Component (WIC) component.
helpviewer_keywords: ["WICAllComponents","WICComponentType","WICComponentType enumeration [Windows Imaging Component]","WICDecoder","WICEncoder","WICMetadataReader","WICMetadataWriter","WICPixelFormat","WICPixelFormatConverter","_wic_codec_wiccomponenttype","wic._wic_codec_wiccomponenttype","wincodec/WICAllComponents","wincodec/WICComponentType","wincodec/WICDecoder","wincodec/WICEncoder","wincodec/WICMetadataReader","wincodec/WICMetadataWriter","wincodec/WICPixelFormat","wincodec/WICPixelFormatConverter"]
old-location: wic\_wic_codec_wiccomponenttype.htm
tech.root: wic
ms.assetid: eff6b77c-ea4b-4476-8d75-dec5bb2e1745
ms.date: 12/05/2018
ms.keywords: WICAllComponents, WICComponentType, WICComponentType enumeration [Windows Imaging Component], WICDecoder, WICEncoder, WICMetadataReader, WICMetadataWriter, WICPixelFormat, WICPixelFormatConverter, _wic_codec_wiccomponenttype, wic._wic_codec_wiccomponenttype, wincodec/WICAllComponents, wincodec/WICComponentType, wincodec/WICDecoder, wincodec/WICEncoder, wincodec/WICMetadataReader, wincodec/WICMetadataWriter, wincodec/WICPixelFormat, wincodec/WICPixelFormatConverter
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: WICComponentType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICComponentType
 - wincodec/WICComponentType
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
 - WICComponentType
---

# WICComponentType enumeration


## -description

Specifies the type of Windows Imaging Component (WIC) component.

## -enum-fields

### -field WICDecoder:0x1

A WIC decoder.

### -field WICEncoder:0x2

A WIC encoder.

### -field WICPixelFormatConverter:0x4

A WIC pixel converter.

### -field WICMetadataReader:0x8

A WIC metadata reader.

### -field WICMetadataWriter:0x10

A WIC metadata writer.

### -field WICPixelFormat:0x20

A WIC pixel format.

### -field WICAllComponents:0x3f

All WIC components.

### -field WICCOMPONENTTYPE_FORCE_DWORD:0x7fffffff

