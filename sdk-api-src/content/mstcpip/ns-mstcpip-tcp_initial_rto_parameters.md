---
UID: NS:mstcpip._TCP_INITIAL_RTO_PARAMETERS
title: TCP_INITIAL_RTO_PARAMETERS (mstcpip.h)
description: Specifies data used by the SIO_TCP_INITIAL_RTO IOCTL to configure initial retransmission timeout (RTO) parameters to be used on the socket.
helpviewer_keywords: ["*PTCP_INITIAL_RTO_PARAMETERS","PTCP_INITIAL_RTO_PARAMETERS","PTCP_INITIAL_RTO_PARAMETERS structure pointer [Winsock]","TCP_INITIAL_RTO_PARAMETERS","TCP_INITIAL_RTO_PARAMETERS structure [Winsock]","mstcpip/PTCP_INITIAL_RTO_PARAMETERS","mstcpip/TCP_INITIAL_RTO_PARAMETERS","winsock.tcp_initial_rto_parameters"]
old-location: winsock\tcp_initial_rto_parameters.htm
tech.root: WinSock
ms.assetid: D8445188-A7D5-4A2C-827A-CB559C3B0748
ms.date: 04/02/2024
ms.keywords: '*PTCP_INITIAL_RTO_PARAMETERS, PTCP_INITIAL_RTO_PARAMETERS, PTCP_INITIAL_RTO_PARAMETERS structure pointer [Winsock], TCP_INITIAL_RTO_PARAMETERS, TCP_INITIAL_RTO_PARAMETERS structure [Winsock], mstcpip/PTCP_INITIAL_RTO_PARAMETERS, mstcpip/TCP_INITIAL_RTO_PARAMETERS, winsock.tcp_initial_rto_parameters'
req.header: mstcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: TCP_INITIAL_RTO_PARAMETERS, *PTCP_INITIAL_RTO_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_INITIAL_RTO_PARAMETERS
 - mstcpip/_TCP_INITIAL_RTO_PARAMETERS
 - PTCP_INITIAL_RTO_PARAMETERS
 - mstcpip/PTCP_INITIAL_RTO_PARAMETERS
 - TCP_INITIAL_RTO_PARAMETERS
 - mstcpip/TCP_INITIAL_RTO_PARAMETERS
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
 - TCP_INITIAL_RTO_PARAMETERS
---

## -description

Specifies data used by the [SIO_TCP_INITIAL_RTO](/windows/win32/winsock/sio-tcp-initial-rto) IOCTL to configure initial retransmission timeout (RTO) parameters to be used on the socket. The Windows TCP/IP stack will honor the values in this struct's members for subsequent connection attempts.

## -struct-fields

### -field Rtt

Supplies the initial round trip time (RTT) estimate in milliseconds. This value is used to compute the retransmission timeout.

### -field MaxSynRetransmissions

Supplies the maximum number of retransmissions that will be attempted before the connection setup fails. The retransmission behavior for TCP is documented in IETF RFC 793 and 2988.

* Use one of the *unspecified* defines **TCP_INITIAL_RTO_UNSPECIFIED_RTT** and **TCP_INITIAL_RTO_UNSPECIFIED_MAX_SYN_RETRANSMISSIONS** to allow the system to pick up administrator-configured settings for the parameter left unspecified.
* You can choose system defaults for any of these fields, and supply those values using the default defines **TCP_INITIAL_RTO_DEFAULT_RTT** and **TCP_INITIAL_RTO_DEFAULT_MAX_SYN_RETRANSMISSIONS**.
* You can use the define **TCP_INITIAL_RTO_NO_SYN_RETRANSMISSIONS** to set the number of SYN retransmissions for a TCP socket to 0 (in other words, the TCP SYN shouldn't be retransmitted).

## -remarks

## -see-also

<a href="/windows/win32/winsock/sio-tcp-initial-rto">SIO_TCP_INITIAL_RTO</a>
