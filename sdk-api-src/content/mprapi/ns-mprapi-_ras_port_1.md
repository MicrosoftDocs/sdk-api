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

# _RAS_PORT_1 structure


## -description


The 
<b>RAS_PORT_1</b> structure contains detailed information regarding a specific RAS port, such as line speed or errors. For more general information about a port, such as port condition or port name, see 
<a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a>.


## -struct-fields




### -field hPort

Handle to the port.


### -field hConnection

Handle to the connection.


### -field dwHardwareCondition

Specifies a 
<a href="https://msdn.microsoft.com/54a92552-9ad2-4a4a-b177-041157b445cd">RAS_HARDWARE_CONDITION</a> structure.


### -field dwLineSpeed

Specifies the line speed of the port, represented in bits per second.


### -field dwBytesXmited

Specifies the bytes transmitted on the port. This value is the number of bytes of compressed data.


### -field dwBytesRcved

Specifies the bytes received on the port. This value is the number of bytes of compressed data.


### -field dwFramesXmited

Specifies the frames transmitted on the port.


### -field dwFramesRcved

Specifies the frames received on the port.


### -field dwCrcErr

Specifies the CRC errors on the port.


### -field dwTimeoutErr

Specifies the time-out errors on the port.


### -field dwAlignmentErr

Specifies the alignment errors on the port.


### -field dwHardwareOverrunErr

Specifies the hardware overrun errors on the port.


### -field dwFramingErr

Specifies the framing errors on the port.


### -field dwBufferOverrunErr

Specifies the buffer overrun errors on the port.


### -field dwCompressionRatioIn

Specifies a percentage that indicates the degree to which data received on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.


### -field dwCompressionRatioOut

Specifies a percentage indicating the degree to which data transmitted on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.


## -see-also




<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS
		  Administration Structures</a>



<a href="https://msdn.microsoft.com/54a92552-9ad2-4a4a-b177-041157b445cd">RAS_HARDWARE_CONDITION</a>



<a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

