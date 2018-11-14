---
UID: NS:mfapi.tagCapturedMetadataISOGains
title: tagCapturedMetadataISOGains
author: windows-sdk-content
description: The CapturedMetadataISOGains structure describes the blob format for MF_CAPTURE_METADATA_ISO_GAINS.
old-location: stream\capturedmetadataisogains.htm
tech.root: stream
ms.assetid: 6B87BDFB-EAD5-496D-BE6A-9AE709119515
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CapturedMetadataISOGains, CapturedMetadataISOGains structure [Streaming Media Devices], mfapi/CapturedMetadataISOGains, stream.capturedmetadataisogains, tagCapturedMetadataISOGains
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - CapturedMetadataISOGains
product: Windows
targetos: Windows
req.typenames: CapturedMetadataISOGains
req.redist: 
---

# tagCapturedMetadataISOGains structure


## -description


The CapturedMetadataISOGains structure describes the blob format for <b>MF_CAPTURE_METADATA_ISO_GAINS</b>.


## -struct-fields




### -field AnalogGain


### -field DigitalGain


## -remarks



The <b>CapturedMetadataISOGains</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_ISO_GAINS</b> attribute.  The metadata item structure for ISO gains (<a href="https://msdn.microsoft.com/B4AC04D7-9F98-41F1-A38D-927F3F3A7699">KSCAMERA_METADATA_ITEMHEADER</a> + ISO gains metadata payload) is up to driver and must be 8-byte aligned.



