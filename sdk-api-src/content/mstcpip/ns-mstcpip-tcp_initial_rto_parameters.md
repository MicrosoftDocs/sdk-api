---
UID: NS:mstcpip._TCP_INITIAL_RTO_PARAMETERS
title: TCP_INITIAL_RTO_PARAMETERS (mstcpip.h)
description: Specifies data used by the SIO_TCP_INITIAL_RTO IOCTL to configure initial re-transmission timeout (RTO) parameters to be used on the socket.
helpviewer_keywords: ["*PTCP_INITIAL_RTO_PARAMETERS","PTCP_INITIAL_RTO_PARAMETERS","PTCP_INITIAL_RTO_PARAMETERS structure pointer [Winsock]","TCP_INITIAL_RTO_PARAMETERS","TCP_INITIAL_RTO_PARAMETERS structure [Winsock]","mstcpip/PTCP_INITIAL_RTO_PARAMETERS","mstcpip/TCP_INITIAL_RTO_PARAMETERS","winsock.tcp_initial_rto_parameters"]
old-location: winsock\tcp_initial_rto_parameters.htm
tech.root: WinSock
ms.assetid: D8445188-A7D5-4A2C-827A-CB559C3B0748
ms.date: 12/05/2018
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

# TCP_INITIAL_RTO_PARAMETERS structure


## -description

The 
<a href="/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers">TCP_INITIAL_RTO_PARAMETERS</a> structure  specifies data used by the <a href="/windows/win32/winsock/sio-tcp-initial-rto">SIO_TCP_INITIAL_RTO</a> IOCTL to configure initial re-transmission timeout (RTO) parameters to be used on the socket.

## -struct-fields

### -field Rtt

Supplies the initial RTT in milliseconds.

### -field MaxSynRetransmissions

Supplies the number of retransmissions attempted before the connection
    setup fails.

## -remarks

The <a href="/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers">TCP_INITIAL_RTO_PARAMETERS</a> structure  allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout. The application can also configure the number of re-transmissions that will be attempted before the connection attempt fails. 

An application should supply the RTT of choice in milliseconds and the maximum number of retransmissions in this structure. The Windows TCP/IP stack will honor these parameters for the subsequent connection attempt. The retransmission behavior for TCP is documented in IETF RFC 793 and 2988.

An application may use the unspecified defines,  <b>TCP_INITIAL_RTO_UNSPECIFIED_RTT</b> and <b>TCP_INITIAL_RTO_UNSPECIFIED_MAX_SYN_RETRANSMISSIONS</b>  when supplying values for one of these fields. This allows the system to pick up administrator configured settings for the parameter left unspecified.

An application can choose system defaults for any of these fields and supply those values using the default defines, <b>TCP_INITIAL_RTO_DEFAULT_RTT</b> and <b>TCP_INITIAL_RTO_DEFAULT_MAX_SYN_RETRANSMISSIONS</b>.

## -see-also

<a href="/windows/win32/winsock/sio-tcp-initial-rto">SIO_TCP_INITIAL_RTO</a>