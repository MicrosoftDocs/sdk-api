---
UID: NE:wincodec.WICBitmapEncoderCacheOption
title: WICBitmapEncoderCacheOption
author: windows-driver-content
description: Specifies the cache options available for an encoder.
old-location: wic\_wic_codec_wicbitmapencodercacheoption.htm
old-project: wic
ms.assetid: cc23cd53-f29b-4e4e-a3d9-038c6f0c5629
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WICBitmapEncoderCacheInMemory, WICBitmapEncoderCacheOption, WICBitmapEncoderCacheOption enumeration [Windows Imaging Component], WICBitmapEncoderCacheTempFile, WICBitmapEncoderNoCache, _wic_codec_wicbitmapencodercacheoption, wic._wic_codec_wicbitmapencodercacheoption, wincodec/WICBitmapEncoderCacheInMemory, wincodec/WICBitmapEncoderCacheOption, wincodec/WICBitmapEncoderCacheTempFile, wincodec/WICBitmapEncoderNoCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICBitmapEncoderCacheOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincodec.h
api_name:
-	WICBitmapEncoderCacheOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



