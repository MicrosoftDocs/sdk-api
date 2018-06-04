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

# _WTS_PROTOCOL_COUNTERS structure


## -description


Contains protocol performance counters.


## -struct-fields




### -field WdBytes

The number of bytes sent and received.


### -field WdFrames

The number of frames sent and received.


### -field WaitForOutBuf

The number of times the protocol waited for an output buffer to become available.


### -field Frames

Transport driver number of frames sent and received.


### -field Bytes

Transport driver number of bytes sent and received.


### -field CompressedBytes

The number of compressed bytes.


### -field CompressFlushes

The number of compressed flushes. A compressed flush occurs when compression for a packet fails and is replaced by the original uncompressed packet.


### -field Errors

The number of packets that were in error during the session.


### -field Timeouts

The number of timeouts during the session.


### -field AsyncFramingError

The number of asynchronous framing errors during the session.


### -field AsyncOverrunError

The number of asynchronous overrun errors during the session.


### -field AsyncOverflowError

The number of asynchronous overflow errors during the session.


### -field AsyncParityError

The number of asynchronous parity errors during the session.


### -field TdErrors

The number of transport protocol errors during the session.


### -field ProtocolType

The type of the protocol.


### -field Length

The length of data in the <b>Reserved</b> field.


### -field Specific

Specifies the type of counter that can be queried. This can be <b>TShareCounters</b> or <b>Reserved</b>.


### -field Reserved

An array of protocol specific data. The maximum length can be WTS_MAX_RESERVED multiplied by the size of an unsigned long integer.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/20e66033-fc79-49c9-af0e-abaf6e4ba501">WTS_PROTOCOL_STATUS</a> structure.



