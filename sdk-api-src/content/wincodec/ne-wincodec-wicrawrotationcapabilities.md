---
UID: NE:wincodec.WICRawRotationCapabilities
title: WICRawRotationCapabilities (wincodec.h)
description: Specifies the rotation capabilities of the codec.
helpviewer_keywords: ["WICRawRotationCapabilities","WICRawRotationCapabilities enumeration [Windows Imaging Component]","WICRawRotationCapabilityFullySupported","WICRawRotationCapabilityGetSupported","WICRawRotationCapabilityNinetyDegreesSupported","WICRawRotationCapabilityNotSupported","_wic_codec_wicrawrotationcapabilities","wic._wic_codec_wicrawrotationcapabilities","wincodec/WICRawRotationCapabilities","wincodec/WICRawRotationCapabilityFullySupported","wincodec/WICRawRotationCapabilityGetSupported","wincodec/WICRawRotationCapabilityNinetyDegreesSupported","wincodec/WICRawRotationCapabilityNotSupported"]
old-location: wic\_wic_codec_wicrawrotationcapabilities.htm
tech.root: wic
ms.assetid: f6713652-7d38-4ac6-80d8-fd53095c50a2
ms.date: 12/05/2018
ms.keywords: WICRawRotationCapabilities, WICRawRotationCapabilities enumeration [Windows Imaging Component], WICRawRotationCapabilityFullySupported, WICRawRotationCapabilityGetSupported, WICRawRotationCapabilityNinetyDegreesSupported, WICRawRotationCapabilityNotSupported, _wic_codec_wicrawrotationcapabilities, wic._wic_codec_wicrawrotationcapabilities, wincodec/WICRawRotationCapabilities, wincodec/WICRawRotationCapabilityFullySupported, wincodec/WICRawRotationCapabilityGetSupported, wincodec/WICRawRotationCapabilityNinetyDegreesSupported, wincodec/WICRawRotationCapabilityNotSupported
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
req.typenames: WICRawRotationCapabilities
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICRawRotationCapabilities
 - wincodec/WICRawRotationCapabilities
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
 - WICRawRotationCapabilities
---

# WICRawRotationCapabilities enumeration


## -description

Specifies the rotation capabilities of the codec.

## -enum-fields

### -field WICRawRotationCapabilityNotSupported:0

Rotation is not supported.

### -field WICRawRotationCapabilityGetSupported:0x1

Set operations for rotation is not supported.

### -field WICRawRotationCapabilityNinetyDegreesSupported:0x2

90 degree rotations are supported.

### -field WICRawRotationCapabilityFullySupported:0x3

All rotation angles are supported.

### -field WICRAWROTATIONCAPABILITIES_FORCE_DWORD:0x7fffffff

