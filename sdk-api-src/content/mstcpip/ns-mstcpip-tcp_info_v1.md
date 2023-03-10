---
UID: NS:mstcpip._TCP_INFO_v1
tech.root: WinSock
title: TCP_INFO_v1
ms.date: 03/01/2021
targetos: Windows
description: Contains the Transmission Control Protocol (TCP) statistics that were collected for a socket. (version 1.0)
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mstcpip.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: TCP_INFO_v1, *PTCP_INFO_v1
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mstcpip.h
api_name:
 - _TCP_INFO_v1
 - PTCP_INFO_v1
 - TCP_INFO_v1
f1_keywords:
 - _TCP_INFO_v1
 - mstcpip/_TCP_INFO_v1
 - PTCP_INFO_v1
 - mstcpip/PTCP_INFO_v1
 - TCP_INFO_v1
 - mstcpip/TCP_INFO_v1
dev_langs:
 - c++
---

## -description

Contains the Transmission Control Protocol (TCP)  statistics that were collected for a socket. Version 1.0 of this structure provides additional fields.

## -struct-fields

### -field State

Contains the Transmission Control Protocol (TCP)  statistics that were collected for a socket.


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

### -field SndLimTransRwin

The number of transitions into the "Receiver Limited" state from either the "Congestion Limited" or "Sender Limited" states. 

### -field SndLimTimeRwin

The cumulative time, in milliseconds, spent in the "Receiver Limited" state where TCP transmission stops because the sender has filled the announced receiver window.

### -field SndLimBytesRwin

The total number of bytes sent in the "Receiver Limited" state.

### -field SndLimTransCwnd

The number of transitions into the "Congestion Limited" state from either the "Receiver Limited" or "Sender Limited" states.

### -field SndLimTimeCwnd

The cumulative time, in milliseconds, spent in the "Congestion Limited" state. When there is a retransmission timeout, it is counted in this member and not the cumulative time for some other state.

### -field SndLimBytesCwnd

The total number of bytes sent in the "Congestion Limited" state.

### -field SndLimTransSnd

The number of transitions into the "Sender Limited" state from either the "Receiver Limited" or "Congestion Limited" states. 

### -field SndLimTimeSnd

The cumulative time, in milliseconds, spent in the "Sender Limited" state.

### -field SndLimBytesSnd

The total number of bytes sent in the "Sender Limited" state.

## -remarks

To get an instance of this structure,  call the 
   <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> or <a href="/previous-versions/windows/hardware/network/ff566296(v=vs.85)">LPWSPIoctl</a> function with the <a href="/windows/win32/winsock/sio-tcp-info">SIO_TCP_INFO</a> 
   control code. Specify 1 for the *lpvInBuffer* field to retrieve the v1 version of this structure.

## -see-also

<a href="/windows/win32/winsock/sio-tcp-info">SIO_TCP_INFO</a>



<a href="/windows/desktop/api/mstcpip/ne-mstcpip-tcpstate">TCPSTATE</a>
