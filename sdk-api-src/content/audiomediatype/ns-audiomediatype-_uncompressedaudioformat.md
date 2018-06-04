---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _UNCOMPRESSEDAUDIOFORMAT structure


## -description


The UNCOMPRESSEDAUDIOFORMAT structure specifies the frame rate, channel mask, and other attributes of the uncompressed audio data format.


## -struct-fields




### -field guidFormatType

Specifies the GUID of the data format type.


### -field dwSamplesPerFrame

Specifies the number of samples per frame.


### -field dwBytesPerSampleContainer

Specifies the number of bytes that make up a unit container of the sample.


### -field dwValidBitsPerSample

Specifies the number of valid bits per sample.


### -field fFramesPerSecond

Specifies the number of frames per second of streaming audio data.


### -field dwChannelMask

Specifies the channel mask that is used by the uncompressed audio data.


## -remarks



This structure provides access to the parameters that describe an uncompressed <a href="http://go.microsoft.com/fwlink/p/?linkid=153892">PCM </a> audio format.



