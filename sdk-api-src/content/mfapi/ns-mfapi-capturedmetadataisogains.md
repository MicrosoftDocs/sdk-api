---
UID: NS:mfapi.tagCapturedMetadataISOGains
title: CapturedMetadataISOGains (mfapi.h)
description: The CapturedMetadataISOGains structure describes the blob format for MF_CAPTURE_METADATA_ISO_GAINS.
helpviewer_keywords: ["CapturedMetadataISOGains","CapturedMetadataISOGains structure [Streaming Media Devices]","mfapi/CapturedMetadataISOGains","stream.capturedmetadataisogains"]
old-location: stream\capturedmetadataisogains.htm
tech.root: stream
ms.assetid: 6B87BDFB-EAD5-496D-BE6A-9AE709119515
ms.date: 12/05/2018
ms.keywords: CapturedMetadataISOGains, CapturedMetadataISOGains structure [Streaming Media Devices], mfapi/CapturedMetadataISOGains, stream.capturedmetadataisogains
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CapturedMetadataISOGains
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCapturedMetadataISOGains
 - mfapi/tagCapturedMetadataISOGains
 - CapturedMetadataISOGains
 - mfapi/CapturedMetadataISOGains
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - CapturedMetadataISOGains
---

# CapturedMetadataISOGains structure


## -description

The CapturedMetadataISOGains structure describes the blob format for <b>MF_CAPTURE_METADATA_ISO_GAINS</b>.

## -struct-fields

### -field AnalogGain

### -field DigitalGain

## -remarks

The <b>CapturedMetadataISOGains</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_ISO_GAINS</b> attribute.  The metadata item structure for ISO gains (<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader">KSCAMERA_METADATA_ITEMHEADER</a> + ISO gains metadata payload) is up to driver and must be 8-byte aligned.