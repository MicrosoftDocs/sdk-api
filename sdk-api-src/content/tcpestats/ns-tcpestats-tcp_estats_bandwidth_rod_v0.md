---
UID: NS:tcpestats._TCP_ESTATS_BANDWIDTH_ROD_v0
title: TCP_ESTATS_BANDWIDTH_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics on bandwidth estimation for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_BANDWIDTH_ROD_v0","PTCP_ESTATS_BANDWIDTH_ROD_v0","PTCP_ESTATS_BANDWIDTH_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_BANDWIDTH_ROD_v0","TCP_ESTATS_BANDWIDTH_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_bandwidth_rod_v0","tcpestats/PTCP_ESTATS_BANDWIDTH_ROD_v0","tcpestats/TCP_ESTATS_BANDWIDTH_ROD_v0"]
old-location: iphlp\tcp_estats_bandwidth_rod_v0.htm
tech.root: IpHlp
ms.assetid: 330d06a2-9966-4e2b-b1bd-44c0f1b9416d
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_BANDWIDTH_ROD_v0, PTCP_ESTATS_BANDWIDTH_ROD_v0, PTCP_ESTATS_BANDWIDTH_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_BANDWIDTH_ROD_v0, TCP_ESTATS_BANDWIDTH_ROD_v0 structure [IP Helper], iphlp.tcp_estats_bandwidth_rod_v0, tcpestats/PTCP_ESTATS_BANDWIDTH_ROD_v0, tcpestats/TCP_ESTATS_BANDWIDTH_ROD_v0'
req.header: tcpestats.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TCP_ESTATS_BANDWIDTH_ROD_v0, *PTCP_ESTATS_BANDWIDTH_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_BANDWIDTH_ROD_v0
 - tcpestats/_TCP_ESTATS_BANDWIDTH_ROD_v0
 - PTCP_ESTATS_BANDWIDTH_ROD_v0
 - tcpestats/PTCP_ESTATS_BANDWIDTH_ROD_v0
 - TCP_ESTATS_BANDWIDTH_ROD_v0
 - tcpestats/TCP_ESTATS_BANDWIDTH_ROD_v0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpestats.h
api_name:
 - TCP_ESTATS_BANDWIDTH_ROD_v0
---

# TCP_ESTATS_BANDWIDTH_ROD_v0 structure


## -description

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on bandwidth estimation for a TCP connection.

## -struct-fields

### -field OutboundBandwidth

Type: <b>ULONG64</b>

The computed outbound bandwidth estimate, in bits per second, for the network path for the TCP connection.

### -field InboundBandwidth

Type: <b>ULONG64</b>

The computed inbound bandwidth estimate, in bits per second, for the network path for the TCP connection.

### -field OutboundInstability

Type: <b>ULONG64</b>

A measure, in bits per second, of the instability of the outbound bandwidth estimate for the network path for the TCP connection.

### -field InboundInstability

Type: <b>ULONG64</b>

A measure, in bits per second, of the instability of the inbound bandwidth estimate for the network path for the TCP connection.

### -field OutboundBandwidthPeaked

Type: <b>BOOLEAN</b>

A boolean value that indicates if the computed outbound bandwidth estimate for the network path for the TCP connection has reached its peak value.

### -field InboundBandwidthPeaked

Type: <b>BOOLEAN</b>

A boolean value that indicates if the computed inbound bandwidth estimate for the network path for the TCP connection has reached its peak value.

## -remarks

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on bandwidth estimation for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsBandwidth</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are not defined in the IETF RFC on the TCP Extended Statistics MIB. For more information on this RFC, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/nldef/ns-nldef-nl_bandwidth_information">NL_BANDWIDTH_INFORMATION</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>