---
UID: NS:wincodecsdk.WICMetadataHeader
title: WICMetadataHeader (wincodecsdk.h)
description: Represents metadata header.
helpviewer_keywords: ["WICMetadataHeader","WICMetadataHeader structure [Windows Imaging Component]","_wic_codec_wicmetadataheader","wic._wic_codec_wicmetadataheader","wincodecsdk/WICMetadataHeader"]
old-location: wic\_wic_codec_wicmetadataheader.htm
tech.root: wic
ms.assetid: f643b163-55b2-4691-a4eb-fc162949e936
ms.date: 12/05/2018
ms.keywords: WICMetadataHeader, WICMetadataHeader structure [Windows Imaging Component], _wic_codec_wicmetadataheader, wic._wic_codec_wicmetadataheader, wincodecsdk/WICMetadataHeader
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
req.typenames: WICMetadataHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICMetadataHeader
 - wincodecsdk/WICMetadataHeader
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
 - WICMetadataHeader
---

# WICMetadataHeader structure


## -description

Represents metadata header.

## -struct-fields

### -field Position

Type: <b>ULARGE_INTEGER</b>

The position of the header.

### -field Length

Type: <b>ULONG</b>

The length of the header.

### -field Header

Type: <b>BYTE*</b>

Pointer to the header.

### -field DataOffset

Type: <b>ULARGE_INTEGER</b>

The offset of the header.

