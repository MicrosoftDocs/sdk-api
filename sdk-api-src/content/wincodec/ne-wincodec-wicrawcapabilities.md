---
UID: NE:wincodec.WICRawCapabilities
title: WICRawCapabilities (wincodec.h)
description: Specifies the capability support of a raw image.
helpviewer_keywords: ["WICRawCapabilities","WICRawCapabilities enumeration [Windows Imaging Component]","WICRawCapabilityFullySupported","WICRawCapabilityGetSupported","WICRawCapabilityNotSupported","_wic_codec_wicrawcapabilities","wic._wic_codec_wicrawcapabilities","wincodec/WICRawCapabilities","wincodec/WICRawCapabilityFullySupported","wincodec/WICRawCapabilityGetSupported","wincodec/WICRawCapabilityNotSupported"]
old-location: wic\_wic_codec_wicrawcapabilities.htm
tech.root: wic
ms.assetid: a82edbbe-a069-4ba8-ba15-524830cdf330
ms.date: 12/05/2018
ms.keywords: WICRawCapabilities, WICRawCapabilities enumeration [Windows Imaging Component], WICRawCapabilityFullySupported, WICRawCapabilityGetSupported, WICRawCapabilityNotSupported, _wic_codec_wicrawcapabilities, wic._wic_codec_wicrawcapabilities, wincodec/WICRawCapabilities, wincodec/WICRawCapabilityFullySupported, wincodec/WICRawCapabilityGetSupported, wincodec/WICRawCapabilityNotSupported
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
req.typenames: WICRawCapabilities
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICRawCapabilities
 - wincodec/WICRawCapabilities
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
 - WICRawCapabilities
---

# WICRawCapabilities enumeration


## -description

Specifies the capability support of a raw image.

## -enum-fields

### -field WICRawCapabilityNotSupported:0

The capability is not supported.

### -field WICRawCapabilityGetSupported:0x1

The capability supports only get operations.

### -field WICRawCapabilityFullySupported:0x2

The capability supports get and set operations.

### -field WICRAWCAPABILITIES_FORCE_DWORD:0x7fffffff

