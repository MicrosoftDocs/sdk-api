---
UID: NS:mstcpip._TCP_INFO_v0
title: TCP_INFO_v0 (mstcpip.h)
description: Contains the Transmission Control Protocol (TCP) statistics that were collected for a socket.
helpviewer_keywords: ["*PTCP_INFO_v0","PTCP_INFO_v0","PTCP_INFO_v0 structure pointer [Winsock]","TCP_INFO_v0","TCP_INFO_v0 structure [Winsock]","mstcpip/PTCP_INFO_v0","mstcpip/TCP_INFO_v0","winsock.tcp_info_v0"]
old-location: winsock\tcp_info_v0.htm
tech.root: WinSock
ms.assetid: 9A51A059-59EC-4D30-9ECE-C81351C0861F
ms.date: 12/05/2018
ms.keywords: '*PTCP_INFO_v0, PTCP_INFO_v0, PTCP_INFO_v0 structure pointer [Winsock], TCP_INFO_v0, TCP_INFO_v0 structure [Winsock], mstcpip/PTCP_INFO_v0, mstcpip/TCP_INFO_v0, winsock.tcp_info_v0'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TCP_INFO_v0, *PTCP_INFO_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_INFO_v0
 - mstcpip/_TCP_INFO_v0
 - PTCP_INFO_v0
 - mstcpip/PTCP_INFO_v0
 - TCP_INFO_v0
 - mstcpip/TCP_INFO_v0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - TCP_INFO_v0
---

# TCP_INFO_v0 structure


## -description

Contains the Transmission Control Protocol (TCP)  statistics that were collected for a socket.

## -struct-fields

### -field State

A value from the <a href="/windows/desktop/api/mstcpip/ne-mstcpip-tcpstate">TCPSTATE</a> enumeration that indicates the  state of the TCP connection.

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

The size of the send window (SND.WND in <a href="https://tools.ietf.org/html/rfc793">RFC 793</a>),  in bytes.

### -field RcvWnd

 The size of the receive window (RCV.WND in <a href="https://tools.ietf.org/html/rfc793">RFC 793</a>), in bytes.

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
   <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> or <a href="/previous-versions/windows/hardware/network/ff566296(v=vs.85)">LPWSPIoctl</a> function with the <a href="/windows/win32/winsock/sio-tcp-info">SIO_TCP_INFO</a> 
   control code. Specify 0 for the *lpvInBuffer* field to retrieve the v0 version of this structure.

## -see-also

<a href="/windows/win32/winsock/sio-tcp-info">SIO_TCP_INFO</a>



<a href="/windows/desktop/api/mstcpip/ne-mstcpip-tcpstate">TCPSTATE</a>
