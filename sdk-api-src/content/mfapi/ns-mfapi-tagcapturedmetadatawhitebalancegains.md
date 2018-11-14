---
UID: NS:mfapi.tagCapturedMetadataWhiteBalanceGains
title: tagCapturedMetadataWhiteBalanceGains
author: windows-sdk-content
description: This structure describes the blob format for the MF_CAPTURE_METADATA_WHITEBALANCE_GAINS attribute.
old-location: stream\capturedmetadatawhitebalancegains.htm
tech.root: stream
ms.assetid: 1F844204-0709-4203-80C5-C90949F96159
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CapturedMetadataWhiteBalanceGains, CapturedMetadataWhiteBalanceGains structure [Streaming Media Devices], mfapi/CapturedMetadataWhiteBalanceGains, stream.capturedmetadatawhitebalancegains, tagCapturedMetadataWhiteBalanceGains
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
 - CapturedMetadataWhiteBalanceGains
product: Windows
targetos: Windows
req.typenames: CapturedMetadataWhiteBalanceGains
req.redist: 
---

# tagCapturedMetadataWhiteBalanceGains structure


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

The <b>CapturedMetadataWhiteBalanceGains</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_WHITEBALANCE_GAINS</b> attribute.  The metadata item structure for white balance gains (<a href="https://msdn.microsoft.com/B4AC04D7-9F98-41F1-A38D-927F3F3A7699">KSCAMERA_METADATA_ITEMHEADER</a> + white balance gains metadata payload) is up to driver and must be 8-byte aligned.



