---
UID: NS:mfapi.tagCapturedMetadataWhiteBalanceGains
title: CapturedMetadataWhiteBalanceGains (mfapi.h)
description: This structure describes the blob format for the MF_CAPTURE_METADATA_WHITEBALANCE_GAINS attribute.
helpviewer_keywords: ["CapturedMetadataWhiteBalanceGains","CapturedMetadataWhiteBalanceGains structure [Streaming Media Devices]","mfapi/CapturedMetadataWhiteBalanceGains","stream.capturedmetadatawhitebalancegains"]
old-location: stream\capturedmetadatawhitebalancegains.htm
tech.root: stream
ms.assetid: 1F844204-0709-4203-80C5-C90949F96159
ms.date: 12/05/2018
ms.keywords: CapturedMetadataWhiteBalanceGains, CapturedMetadataWhiteBalanceGains structure [Streaming Media Devices], mfapi/CapturedMetadataWhiteBalanceGains, stream.capturedmetadatawhitebalancegains
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
req.typenames: CapturedMetadataWhiteBalanceGains
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCapturedMetadataWhiteBalanceGains
 - mfapi/tagCapturedMetadataWhiteBalanceGains
 - CapturedMetadataWhiteBalanceGains
 - mfapi/CapturedMetadataWhiteBalanceGains
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
 - CapturedMetadataWhiteBalanceGains
---

# CapturedMetadataWhiteBalanceGains structure


## -description

This structure describes the blob format for the <b>MF_CAPTURE_METADATA_WHITEBALANCE_GAINS</b> attribute.

## -struct-fields

### -field R

The  <b>R</b> value of the blob.

### -field G

The  <b>G</b> value of the blob.

### -field B

The  <b>B</b> value of the blob.

## -remarks

The <b>MF_CAPTURE_METADATA_WHITEBALANCE_GAINS</b> attribute contains the white balance gains applied to R, G, B by the sensor or ISP when the preview frame was captured. This is a unitless.

The <b>CapturedMetadataWhiteBalanceGains</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_WHITEBALANCE_GAINS</b> attribute.  The metadata item structure for white balance gains (<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader">KSCAMERA_METADATA_ITEMHEADER</a> + white balance gains metadata payload) is up to driver and must be 8-byte aligned.