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

# _TCP_INFO_v0 structure


## -description


Contains the Transmission Control Protocol (TCP)  statistics that were collected for a socket.


## -struct-fields




### -field State

A value from the <a href="https://msdn.microsoft.com/225C423E-C820-4E9F-8261-DA1E14F81683">TCPSTATE</a> enumeration that indicates the  state of the TCP connection.


### -field Mss

The current maximum segment size (MSS) for the connection, in bytes.


### -field ConnectionTimeMs

The lifetime of the connection, in milliseconds.


### -field TimestampsEnabled

<b>TRUE</b> if TCP time stamps are turned on for the connection; otherwise <b>FALSE</b>.


### -field RttUs

The current estimated round-trip time for the connection, in microseconds.


### -field MinRttUs

The minimum sampled round trip time, in microseconds.


### -field BytesInFlight

The current number of sent bytes that are unacknowledged.


### -field Cwnd

The size of the current congestion window, in bytes.


### -field SndWnd

The size of the send window (SND.WND in <a href="https://go.microsoft.com/fwlink/p/?linkid=852445">RFC 793</a>),  in bytes. 


### -field RcvWnd

 The size of the receive window (RCV.WND in <a href="https://go.microsoft.com/fwlink/p/?linkid=852445">RFC 793</a>), in bytes.


### -field RcvBuf

The size of the current receive buffer, in bytes.   The size of the receive buffer  changes dynamically when autotuning is turned on for the receive window.


### -field BytesOut

The total number of bytes sent.


### -field BytesIn

The total number of bytes received.


### -field BytesReordered

The total number of bytes reordered.


### -field BytesRetrans

The total number of bytes retransmitted.


### -field FastRetrans

The number of calls of the Fast Retransmit algorithm.


### -field DupAcksIn

The total number of duplicate acknowledgments received.


### -field TimeoutEpisodes

The total number of retransmission timeout episodes. Each episode can consist of multiple timeouts.


### -field SynRetrans

The total number of retransmitted synchronize control flags (SYNs).


## -remarks



To get an instance of this structure,  call the 
   <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a> function with the <a href="https://msdn.microsoft.com/AB5F25B6-D2D2-42D7-8189-06CAC4842C66">SIO_TCP_INFO</a> 
   control code.




## -see-also




<a href="https://msdn.microsoft.com/AB5F25B6-D2D2-42D7-8189-06CAC4842C66">SIO_TCP_INFO</a>



<a href="https://msdn.microsoft.com/225C423E-C820-4E9F-8261-DA1E14F81683">TCPSTATE</a>
 

 

