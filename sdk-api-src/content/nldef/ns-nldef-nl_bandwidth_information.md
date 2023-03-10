---
UID: NS:nldef._NL_BANDWIDTH_INFORMATION
title: NL_BANDWIDTH_INFORMATION (nldef.h)
description: Contains read-only information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.
helpviewer_keywords: ["*PNL_BANDWIDTH_INFORMATION","NL_BANDWIDTH_INFORMATION","NL_BANDWIDTH_INFORMATION structure [IP Helper]","PNL_BANDWIDTH_INFORMATION","PNL_BANDWIDTH_INFORMATION structure pointer [IP Helper]","iphlp.nl_bandwidth_information","nldef/NL_BANDWIDTH_INFORMATION","nldef/PNL_BANDWIDTH_INFORMATION"]
old-location: iphlp\nl_bandwidth_information.htm
tech.root: IpHlp
ms.assetid: F5D7238A-EAE0-4D60-A0A4-D839F738EF48
ms.date: 12/05/2018
ms.keywords: '*PNL_BANDWIDTH_INFORMATION, NL_BANDWIDTH_INFORMATION, NL_BANDWIDTH_INFORMATION structure [IP Helper], PNL_BANDWIDTH_INFORMATION, PNL_BANDWIDTH_INFORMATION structure pointer [IP Helper], iphlp.nl_bandwidth_information, nldef/NL_BANDWIDTH_INFORMATION, nldef/PNL_BANDWIDTH_INFORMATION'
req.header: nldef.h
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
req.typenames: NL_BANDWIDTH_INFORMATION, *PNL_BANDWIDTH_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NL_BANDWIDTH_INFORMATION
 - nldef/_NL_BANDWIDTH_INFORMATION
 - PNL_BANDWIDTH_INFORMATION
 - nldef/PNL_BANDWIDTH_INFORMATION
 - NL_BANDWIDTH_INFORMATION
 - nldef/NL_BANDWIDTH_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nldef.h
api_name:
 - NL_BANDWIDTH_INFORMATION
---

# NL_BANDWIDTH_INFORMATION structure


## -description

The <b>NL_BANDWIDTH_INFORMATION</b> structure contains read-only information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.

## -struct-fields

### -field Bandwidth

The estimated maximum available bandwidth, in bits per second.

### -field Instability

A measure of the variation based on recent bandwidth samples, in bits per second.

### -field BandwidthPeaked

A value that indicates if the bandwidth estimate in the <b>Bandwidth</b> member has peaked and reached its maximum value for the given network conditions. 

The TCP/IP stack uses a heuristic to set this variable. Until this variable is set, there is no guarantee that the true available maximum bandwidth is not higher than the estimated bandwidth in the <b>Bandwidth</b> member. However, it is safe to assume that maximum available bandwidth is not lower than the estimate reported in the <b>Bandwidth</b> member.

## -remarks

The  <b>NL_BANDWIDTH_INFORMATION</b> structure is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Nldef.h</i> and <i>Iptypes.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/win32/api/netioapi/ns-netioapi-mib_ip_network_connection_bandwidth_estimates">MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rod_v0">TCP_ESTATS_BANDWIDTH_ROD_v0</a>