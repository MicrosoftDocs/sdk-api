---
UID: NF:netioapi.GetIpNetworkConnectionBandwidthEstimates
title: GetIpNetworkConnectionBandwidthEstimates function (netioapi.h)
description: Retrieves historical bandwidth estimates for a network connection on the specified interface.
helpviewer_keywords: ["AF_INET","AF_INET6","GetIpNetworkConnectionBandwidthEstimates","GetIpNetworkConnectionBandwidthEstimates function [IP Helper]","iphlp.getipnetworkconnectionbandwidthestimates","netioapi/GetIpNetworkConnectionBandwidthEstimates"]
old-location: iphlp\getipnetworkconnectionbandwidthestimates.htm
tech.root: IpHlp
ms.assetid: FE60AF0D-15B0-4223-8AE1-3E65483A1C5F
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetIpNetworkConnectionBandwidthEstimates, GetIpNetworkConnectionBandwidthEstimates function [IP Helper], iphlp.getipnetworkconnectionbandwidthestimates, netioapi/GetIpNetworkConnectionBandwidthEstimates
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIpNetworkConnectionBandwidthEstimates
 - netioapi/GetIpNetworkConnectionBandwidthEstimates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpNetworkConnectionBandwidthEstimates
---

# GetIpNetworkConnectionBandwidthEstimates function


## -description

The 
<b>GetIpNetworkConnectionBandwidthEstimates</b> function  retrieves historical bandwidth estimates for a  network connection on the specified interface.

## -parameters

### -param InterfaceIndex [in]

The local index value for the network interface. 

This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -param AddressFamily [in]

The address family. Possible values for the address family are listed in the <i>Ws2def.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

 Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b> or <b>AF_INET6</b>, which are the Internet
                     address family formats for IPv4 and IPv6. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family.

</td>
</tr>
</table>

### -param BandwidthEstimates [out]

A pointer to a buffer that returns the historical bandwidth estimates maintained for the point of attachment to which the interface is currently connected.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  interface index specified by the <i>InterfaceIndex</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>BandwidthEstimates</i> parameter or the <i>AddressFamily</i> parameter was not specified as <b>AF_INET</b> or <b>AF_INET6</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <i>InterfaceIndex</i> parameter does not match the IP address family specified in the <i>AddressFamily</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetIpNetworkConnectionBandwidthEstimates</b> function is defined on Windows 8  and later. 

On input, the <i>AddressFamily</i> parameter must be initialized to either <b>AF_INET</b> or <b>AF_INET6</b>. In addition on input, the <i>InterfaceIndex</i> parameter must be initialized with the specified interface index.

A value must be set for the  <i>InterfaceIndex</i> parameter (the value of this parameter must not be set to zero). 

On output, the <a href="/windows/win32/api/netioapi/ns-netioapi-mib_ip_network_connection_bandwidth_estimates">MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</a>  structure pointed to by the <i>BandwidthEstimates</i> parameter is filled in if the <i>AddressFamily</i> and <i>InterfaceIndex</i> parameters were specified. 

The <b>GetIpNetworkConnectionBandwidthEstimates</b> function returns historical estimates of available bandwidth at the point of attachment (the first hop) for use by an application. The estimates are intended as a guide to tune performance parameters and the application should maintain thresholds and differentiate behavior for low and high bandwidth situations. 

It is possible that the true available bandwidth changes over  time as more bandwidth is consumed by devices competing on the same network. So applications should be prepared to handle cases where the available bandwidth drops below historical limits reported by the <b>GetIpNetworkConnectionBandwidthEstimates</b> function. 

It is possible that the TCP/IP stack has not built up any estimates for the given interface,  in a particular or both directions. In this case the estimate returned will be zero. The application should be prepared to handle such cases by picking reasonable defaults and fine tuning if required.

The <i>Netioapi.h</i> header file is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/win32/api/netioapi/ns-netioapi-mib_ip_network_connection_bandwidth_estimates">MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</a>



<a href="/windows/desktop/api/nldef/ns-nldef-nl_bandwidth_information">NL_BANDWIDTH_INFORMATION</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rod_v0">TCP_ESTATS_BANDWIDTH_ROD_v0</a>