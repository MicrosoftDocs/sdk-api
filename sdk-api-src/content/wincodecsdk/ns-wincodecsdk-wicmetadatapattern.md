---
UID: NS:wincodecsdk.WICMetadataPattern
title: WICMetadataPattern (wincodecsdk.h)
description: Represents a metadata pattern.
helpviewer_keywords: ["WICMetadataPattern","WICMetadataPattern structure [Windows Imaging Component]","_wic_codec_wicmetadatapattern","wic._wic_codec_wicmetadatapattern","wincodecsdk/WICMetadataPattern"]
old-location: wic\_wic_codec_wicmetadatapattern.htm
tech.root: wic
ms.assetid: cea9e07d-5e55-4320-9744-b5864b58cfd6
ms.date: 12/05/2018
ms.keywords: WICMetadataPattern, WICMetadataPattern structure [Windows Imaging Component], _wic_codec_wicmetadatapattern, wic._wic_codec_wicmetadatapattern, wincodecsdk/WICMetadataPattern
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICMetadataPattern
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICMetadataPattern
 - wincodecsdk/WICMetadataPattern
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodecsdk.h
api_name:
 - WICMetadataPattern
---

# WICMetadataPattern structure


## -description

Represents a metadata pattern.

## -struct-fields

### -field Position

Type: <b>ULARGE_INTEGER</b>

The position of the pattern.

### -field Length

Type: <b>ULONG</b>

The length of the pattern.

### -field Pattern

Type: <b>BYTE*</b>

Pointer to the pattern.

### -field Mask

Type: <b>BYTE*</b>

Pointer to the pattern mask.

### -field DataOffset

Type: <b>ULARGE_INTEGER</b>

The offset location of the pattern.

