---
UID: NE:mstcpip._TCPSTATE
title: TCPSTATE (mstcpip.h)
description: Indicates the possible states of a Transmission Control Protocol (TCP) connection.
helpviewer_keywords: ["TCPSTATE","TCPSTATE enumeration [Winsock]","TCPSTATE_CLOSED","TCPSTATE_CLOSE_WAIT","TCPSTATE_CLOSING","TCPSTATE_ESTABLISHED","TCPSTATE_FIN_WAIT_1","TCPSTATE_FIN_WAIT_2","TCPSTATE_LAST_ACK","TCPSTATE_LISTEN","TCPSTATE_MAX","TCPSTATE_SYN_RCVD","TCPSTATE_SYN_SENT","TCPSTATE_TIME_WAIT","mstcpip/TCPSTATE","mstcpip/TCPSTATE_CLOSED","mstcpip/TCPSTATE_CLOSE_WAIT","mstcpip/TCPSTATE_CLOSING","mstcpip/TCPSTATE_ESTABLISHED","mstcpip/TCPSTATE_FIN_WAIT_1","mstcpip/TCPSTATE_FIN_WAIT_2","mstcpip/TCPSTATE_LAST_ACK","mstcpip/TCPSTATE_LISTEN","mstcpip/TCPSTATE_MAX","mstcpip/TCPSTATE_SYN_RCVD","mstcpip/TCPSTATE_SYN_SENT","mstcpip/TCPSTATE_TIME_WAIT","winsock.tcpstate"]
old-location: winsock\tcpstate.htm
tech.root: WinSock
ms.assetid: 225C423E-C820-4E9F-8261-DA1E14F81683
ms.date: 12/05/2018
ms.keywords: TCPSTATE, TCPSTATE enumeration [Winsock], TCPSTATE_CLOSED, TCPSTATE_CLOSE_WAIT, TCPSTATE_CLOSING, TCPSTATE_ESTABLISHED, TCPSTATE_FIN_WAIT_1, TCPSTATE_FIN_WAIT_2, TCPSTATE_LAST_ACK, TCPSTATE_LISTEN, TCPSTATE_MAX, TCPSTATE_SYN_RCVD, TCPSTATE_SYN_SENT, TCPSTATE_TIME_WAIT, mstcpip/TCPSTATE, mstcpip/TCPSTATE_CLOSED, mstcpip/TCPSTATE_CLOSE_WAIT, mstcpip/TCPSTATE_CLOSING, mstcpip/TCPSTATE_ESTABLISHED, mstcpip/TCPSTATE_FIN_WAIT_1, mstcpip/TCPSTATE_FIN_WAIT_2, mstcpip/TCPSTATE_LAST_ACK, mstcpip/TCPSTATE_LISTEN, mstcpip/TCPSTATE_MAX, mstcpip/TCPSTATE_SYN_RCVD, mstcpip/TCPSTATE_SYN_SENT, mstcpip/TCPSTATE_TIME_WAIT, winsock.tcpstate
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
req.typenames: TCPSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCPSTATE
 - mstcpip/_TCPSTATE
 - TCPSTATE
 - mstcpip/TCPSTATE
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
 - TCPSTATE
---

# TCPSTATE enumeration


## -description

The Windows Sockets 
<b>TCPSTATE</b> enumeration indicates the possible states of a Transmission Control Protocol (TCP) connection.

## -enum-fields

### -field TCPSTATE_CLOSED

The TCP connection has no connection state at all. This state represents the state when there is no Transmission Control Block (TCB), and therefore,
  no connection.

### -field TCPSTATE_LISTEN

The TCP connection is waiting for a connection request from any remote
    TCP and port.

### -field TCPSTATE_SYN_SENT

-The TCP connection is waiting for a matching connection request
    after sending a connection request.

### -field TCPSTATE_SYN_RCVD

The TCP connection is waiting for an acknowledgment that confirms the connection
    request after both receiving and sending a
    connection request.

### -field TCPSTATE_ESTABLISHED

The TCP connection is an open connection, so the data received can be
    delivered to the user.  This state is normal state for the data transfer phase
    of the connection.

### -field TCPSTATE_FIN_WAIT_1

The TCP connection is waiting for a request to end the connection 
    from the remote TCP, or an acknowledgment of the previously sent request to end the connection.

### -field TCPSTATE_FIN_WAIT_2

The TCP connection is  waiting for a request to end the connection
    from the remote TCP.

### -field TCPSTATE_CLOSE_WAIT

The TCP connection is waiting for a request to end the connection
    from the local user.

### -field TCPSTATE_CLOSING

The TCP connection is waiting for an acknowledgment of the  request to end the connection from the remote TCP.

### -field TCPSTATE_LAST_ACK

The TCP connection is waiting for an acknowledgment of the request to end the connection that was previously sent to the remote TCP, which includes an acknowledgment of its request to end the connection.

### -field TCPSTATE_TIME_WAIT

The TCP connection is waiting for enough time to pass to be sure
    the remote TCP received the acknowledgment of its request to end the connection.

### -field TCPSTATE_MAX

The maximum value of the <a href="/windows/desktop/api/mstcpip/ne-mstcpip-tcpstate">TCPSTATE</a> enumeration.

## -remarks

A TCP connection progresses from one state to another in response to
  events.  The events are the user calls OPEN, SEND, RECEIVE, CLOSE,
  ABORT, and STATUS; the incoming segments, particularly those
  containing the SYN, ACK, RST and FIN flags; and timeouts.

For more information about TCP connection states, see <a href="https://tools.ietf.org/html/rfc793">RFC 793</a>.

## -see-also

<a href="/windows/win32/winsock/sio-tcp-info">SIO_TCP_INFO</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0">TCP_INFO_v0</a>