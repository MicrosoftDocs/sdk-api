---
UID: NE:wincodec.WICDdsAlphaMode
title: WICDdsAlphaMode (wincodec.h)
description: Specifies the the meaning of pixel color component values contained in the DDS image.
helpviewer_keywords: ["WICDdsAlphaMode","WICDdsAlphaMode enumeration [Windows Imaging Component]","WICDdsAlphaModeCustom","WICDdsAlphaModeOpaque","WICDdsAlphaModePremultiplied","WICDdsAlphaModeStraight","WICDdsAlphaModeUnknown","wic.wicddsalphamode","wincodec/WICDdsAlphaMode","wincodec/WICDdsAlphaModeCustom","wincodec/WICDdsAlphaModeOpaque","wincodec/WICDdsAlphaModePremultiplied","wincodec/WICDdsAlphaModeStraight","wincodec/WICDdsAlphaModeUnknown"]
old-location: wic\wicddsalphamode.htm
tech.root: wic
ms.assetid: 67C9B07F-5259-4032-9EBF-CBC3B8637343
ms.date: 12/05/2018
ms.keywords: WICDdsAlphaMode, WICDdsAlphaMode enumeration [Windows Imaging Component], WICDdsAlphaModeCustom, WICDdsAlphaModeOpaque, WICDdsAlphaModePremultiplied, WICDdsAlphaModeStraight, WICDdsAlphaModeUnknown, wic.wicddsalphamode, wincodec/WICDdsAlphaMode, wincodec/WICDdsAlphaModeCustom, wincodec/WICDdsAlphaModeOpaque, wincodec/WICDdsAlphaModePremultiplied, wincodec/WICDdsAlphaModeStraight, wincodec/WICDdsAlphaModeUnknown
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: WICDdsAlphaMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICDdsAlphaMode
 - wincodec/WICDdsAlphaMode
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
 - WICDdsAlphaMode
---

# WICDdsAlphaMode enumeration


## -description

Specifies the the meaning of pixel color component values contained in the DDS image.

## -enum-fields

### -field WICDdsAlphaModeUnknown:0

Alpha behavior is unspecified and must be determined by the reader.

### -field WICDdsAlphaModeStraight:0x1

The alpha data is straight.

### -field WICDdsAlphaModePremultiplied:0x2

The alpha data is premultiplied.

### -field WICDdsAlphaModeOpaque:0x3

The alpha data is opaque (UNORM value of 1). This can be used by a compliant reader as a performance optimization. For example, blending operations can be converted to copies.

### -field WICDdsAlphaModeCustom:0x4

The alpha channel contains custom data that is not alpha.

### -field WICDDSALPHAMODE_FORCE_DWORD:0x7fffffff

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getparameters">IWICDdsDecoder::GetParameters</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>
