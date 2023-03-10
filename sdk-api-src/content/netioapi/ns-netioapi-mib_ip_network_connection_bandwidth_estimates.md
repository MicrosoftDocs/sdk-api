---
UID: NS:netioapi._MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
title: MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES (netioapi.h)
description: Contains read-only information for the bandwidth estimates computed by the TCP/IP stack for a network connection.
helpviewer_keywords: ["*PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES","MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES","MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure [MIB]","PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES","PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure pointer [MIB]","mib.mib_ip_network_connection_bandwidth_estimates","netioapi/MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES","netioapi/PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES"]
old-location: mib\mib_ip_network_connection_bandwidth_estimates.htm
tech.root: MIB
ms.assetid: E3109F71-E103-4586-9274-B83C4DC22382
ms.date: 12/05/2018
ms.keywords: '*PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure [MIB], PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure pointer [MIB], mib.mib_ip_network_connection_bandwidth_estimates, netioapi/MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, netioapi/PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES'
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.typenames: MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, *PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
 - netioapi/_MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
 - PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
 - netioapi/PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
 - MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
 - netioapi/MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
---

# MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure


## -description

The 
<b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure contains read-only information for the bandwidth estimates computed by the TCP/IP stack for a network connection.

## -struct-fields

### -field InboundBandwidthInformation

Bandwidth estimates for the data being received by the host from the IP network.

### -field OutboundBandwidthInformation

Bandwidth estimates for the data being sent from the host to the IP network.

## -remarks

The 
<b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure provides bandwidth estimates computed by the TCP/IP stack for a network connection. These bandwidth estimates are for the point of attachment of the host system to the underlying IP network. 

The <b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure is used with the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates">GetIpNetworkConnectionBandwidthEstimates</a> function to return bandwidth estimates obtained for the point of attachment to the IP network. It is possible to have asymmetric deployments and network conditions where the estimates observed inbound and outbound differ from each other.

The  <b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b>  structure is defined in the <i>Netioapi.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/nldef/ns-nldef-nl_bandwidth_information">NL_BANDWIDTH_INFORMATION</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rod_v0">TCP_ESTATS_BANDWIDTH_ROD_v0</a>