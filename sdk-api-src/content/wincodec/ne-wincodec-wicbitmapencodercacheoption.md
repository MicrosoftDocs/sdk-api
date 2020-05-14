---
UID: NE:wincodec.WICBitmapEncoderCacheOption
title: WICBitmapEncoderCacheOption (wincodec.h)
description: Specifies the cache options available for an encoder.helpviewer_keywords: ["WICBitmapEncoderCacheInMemory","WICBitmapEncoderCacheOption","WICBitmapEncoderCacheOption enumeration [Windows Imaging Component]","WICBitmapEncoderCacheTempFile","WICBitmapEncoderNoCache","_wic_codec_wicbitmapencodercacheoption","wic._wic_codec_wicbitmapencodercacheoption","wincodec/WICBitmapEncoderCacheInMemory","wincodec/WICBitmapEncoderCacheOption","wincodec/WICBitmapEncoderCacheTempFile","wincodec/WICBitmapEncoderNoCache"]
old-location: wic\_wic_codec_wicbitmapencodercacheoption.htm
tech.root: wic
ms.assetid: cc23cd53-f29b-4e4e-a3d9-038c6f0c5629
ms.date: 12/05/2018
ms.keywords: WICBitmapEncoderCacheInMemory, WICBitmapEncoderCacheOption, WICBitmapEncoderCacheOption enumeration [Windows Imaging Component], WICBitmapEncoderCacheTempFile, WICBitmapEncoderNoCache, _wic_codec_wicbitmapencodercacheoption, wic._wic_codec_wicbitmapencodercacheoption, wincodec/WICBitmapEncoderCacheInMemory, wincodec/WICBitmapEncoderCacheOption, wincodec/WICBitmapEncoderCacheTempFile, wincodec/WICBitmapEncoderNoCache
f1_keywords:
- wincodec/WICBitmapEncoderCacheOption
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincodec.h
api_name:
- WICBitmapEncoderCacheOption
targetos: Windows
req.typenames: WICBitmapEncoderCacheOption
req.redist: 
ms.custom: 19H1
---

# WICBitmapEncoderCacheOption enumeration


## -description


Specifies the cache options available for an encoder.


## -enum-fields




### -field WICBitmapEncoderCacheInMemory

The encoder is cached in memory. This option is not supported.


### -field WICBitmapEncoderCacheTempFile

The encoder is cached to a temporary file. This option is not supported.


### -field WICBitmapEncoderNoCache

The encoder is not cached.


### -field WICBITMAPENCODERCACHEOPTION_FORCE_DWORD



