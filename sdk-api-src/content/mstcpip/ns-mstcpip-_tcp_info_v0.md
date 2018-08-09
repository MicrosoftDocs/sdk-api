---
UID: NS:mstcpip._TCP_INFO_v0
title: "_TCP_INFO_v0"
author: windows-sdk-content
description: Contains the Transmission Control Protocol (TCP) statistics that were collected for a socket.
old-location: winsock\tcp_info_v0.htm
old-project: winsock
ms.assetid: 9A51A059-59EC-4D30-9ECE-C81351C0861F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PTCP_INFO_v0, PTCP_INFO_v0, PTCP_INFO_v0 structure pointer [Winsock], TCP_INFO_v0, TCP_INFO_v0 structure [Winsock], _TCP_INFO_v0, mstcpip/PTCP_INFO_v0, mstcpip/TCP_INFO_v0, winsock.tcp_info_v0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: TCP_INFO_v0, *PTCP_INFO_v0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - TCP_INFO_v0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

