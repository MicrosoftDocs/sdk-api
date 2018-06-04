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

# _RAS_CONNECTION_1 structure


## -description


The 
<b>RAS_CONNECTION_1</b> structure contains detailed information regarding a specific connection, such as error counts and bytes received. For more general information about a specific connection, such as user name or domain, see 
<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>.


## -struct-fields




### -field hConnection

A handle to the connection.


### -field hInterface

A handle to the interface.


### -field PppInfo

A <a href="https://msdn.microsoft.com/39692a38-ab40-43da-a704-8c206be72ceb">PPP_INFO</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.


### -field dwBytesXmited

A value that specifies the number of bytes transmitted on the connection.


### -field dwBytesRcved

A value that specifies the number of bytes received on the connection. 


### -field dwFramesXmited

A value that specifies the number of frames transmitted on the connection. 


### -field dwFramesRcved

A value that specifies the number of frames received on the connection. 


### -field dwCrcErr

A value that specifies the number of Cyclic Redundancy Check (CRC) errors on the connection.


### -field dwTimeoutErr

A value that specifies the number of time-out errors on the connection. 


### -field dwAlignmentErr

A value that specifies the number of alignment errors on the connection. 


### -field dwHardwareOverrunErr

A value that specifies the number of hardware overrun errors on the connection. 


### -field dwFramingErr

A value that specifies the number of framing errors on the connection.


### -field dwBufferOverrunErr

A value that specifies the number of buffer overrun errors on the connection.


### -field dwCompressionRatioIn

A value that specifies the percentage by which data received on this connection is compressed. <b>dwCompressionRatioIn</b> is the size of the compressed data divided by the size of the same data in an uncompressed state.


### -field dwCompressionRatioOut

A value that specifies the percentage by which data transmitted on this connection is compressed. The ratio is the size of the compressed data divided by the size of the same data in an uncompressed state.


## -see-also




<a href="https://msdn.microsoft.com/58fea0ca-b7c1-4d32-bcfc-10b41e101f30">MprAdminAcceptReauthentication</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/8c31d345-8f57-47f5-a021-e399f7ccca5d">MprAdminConnectionHangupNotification3</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

