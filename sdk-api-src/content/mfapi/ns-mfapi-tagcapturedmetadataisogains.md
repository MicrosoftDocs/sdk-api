---
UID: NS:mfapi.tagCapturedMetadataISOGains
title: tagCapturedMetadataISOGains
author: windows-sdk-content
description: The CapturedMetadataISOGains structure describes the blob format for MF_CAPTURE_METADATA_ISO_GAINS.
old-location: stream\capturedmetadataisogains.htm
old-project: stream
ms.assetid: 6B87BDFB-EAD5-496D-BE6A-9AE709119515
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: CapturedMetadataISOGains, CapturedMetadataISOGains structure [Streaming Media Devices], mfapi/CapturedMetadataISOGains, stream.capturedmetadataisogains, tagCapturedMetadataISOGains
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CapturedMetadataISOGains
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagCapturedMetadataISOGains structure


## -description


The CapturedMetadataISOGains structure describes the blob format for <b>MF_CAPTURE_METADATA_ISO_GAINS</b>.


## -struct-fields




### -field AnalogGain


### -field DigitalGain


## -remarks



The <b>CapturedMetadataISOGains</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_ISO_GAINS</b> attribute.  The metadata item structure for ISO gains (<a href="https://msdn.microsoft.com/library/windows/hardware/dn925184">KSCAMERA_METADATA_ITEMHEADER</a> + ISO gains metadata payload) is up to driver and must be 8-byte aligned.



