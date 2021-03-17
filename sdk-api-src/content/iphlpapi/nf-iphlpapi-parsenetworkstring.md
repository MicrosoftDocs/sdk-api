---
UID: NF:iphlpapi.ParseNetworkString
title: ParseNetworkString function (iphlpapi.h)
description: Parses the input network string and checks whether it is a legal representation of the specified IP network string type. If the string matches a type and its specification, the function can optionally return the parsed result.
helpviewer_keywords: ["NET_STRING_ANY_ADDRESS","NET_STRING_ANY_ADDRESS_NO_SCOPE","NET_STRING_ANY_SERVICE","NET_STRING_ANY_SERVICE_NO_SCOPE","NET_STRING_IPV4_ADDRESS","NET_STRING_IPV4_NETWORK","NET_STRING_IPV4_SERVICE","NET_STRING_IPV6_ADDRESS","NET_STRING_IPV6_ADDRESS_NO_SCOPE","NET_STRING_IPV6_NETWORK","NET_STRING_IPV6_SERVICE","NET_STRING_IPV6_SERVICE_NO_SCOPE","NET_STRING_IP_ADDRESS","NET_STRING_IP_ADDRESS_NO_SCOPE","NET_STRING_IP_NETWORK","NET_STRING_IP_SERVICE","NET_STRING_IP_SERVICE_NO_SCOPE","NET_STRING_NAMED_ADDRESS","NET_STRING_NAMED_SERVICE","ParseNetworkString","ParseNetworkString function [IP Helper]","iphlp.parsenetworkstring","iphlpapi/ParseNetworkString"]
old-location: iphlp\parsenetworkstring.htm
tech.root: IpHlp
ms.assetid: 43bc866f-7776-4f59-9ed6-4c6fc4da7f83
ms.date: 12/05/2018
ms.keywords: NET_STRING_ANY_ADDRESS, NET_STRING_ANY_ADDRESS_NO_SCOPE, NET_STRING_ANY_SERVICE, NET_STRING_ANY_SERVICE_NO_SCOPE, NET_STRING_IPV4_ADDRESS, NET_STRING_IPV4_NETWORK, NET_STRING_IPV4_SERVICE, NET_STRING_IPV6_ADDRESS, NET_STRING_IPV6_ADDRESS_NO_SCOPE, NET_STRING_IPV6_NETWORK, NET_STRING_IPV6_SERVICE, NET_STRING_IPV6_SERVICE_NO_SCOPE, NET_STRING_IP_ADDRESS, NET_STRING_IP_ADDRESS_NO_SCOPE, NET_STRING_IP_NETWORK, NET_STRING_IP_SERVICE, NET_STRING_IP_SERVICE_NO_SCOPE, NET_STRING_NAMED_ADDRESS, NET_STRING_NAMED_SERVICE, ParseNetworkString, ParseNetworkString function [IP Helper], iphlp.parsenetworkstring, iphlpapi/ParseNetworkString
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ParseNetworkString
 - iphlpapi/ParseNetworkString
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
 - ParseNetworkString
---

# ParseNetworkString function


## -description

The 
<b>ParseNetworkString</b> function  parses the input network string and checks whether it
    is a legal representation of the specified IP network string type. If the string matches a type and its specification,
    the function can optionally return the parsed result.

## -parameters

### -param NetworkString [in]

A pointer to the NULL-terminated network string to parse.

### -param Types [in]

The type of IP network string to parse. This parameter consists of one of network string types as defined in the <i>Iphlpapi.h</i> 
        header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV4_ADDRESS"></a><a id="net_string_ipv4_address"></a><dl>
<dt><b>NET_STRING_IPV4_ADDRESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 address using Internet standard dotted-decimal notation.
   A network port or prefix must not be present in the network string. 

An example network string is the following:

<b>192.168.100.10</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV4_SERVICE"></a><a id="net_string_ipv4_service"></a><dl>
<dt><b>NET_STRING_IPV4_SERVICE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 service using Internet standard dotted-decimal notation.
   A network port is required as part of the network string. A prefix must not be present in the network string. 

An example network string is the following:

<b>192.168.100.10:80</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV4_NETWORK"></a><a id="net_string_ipv4_network"></a><dl>
<dt><b>NET_STRING_IPV4_NETWORK</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 network using Internet standard dotted-decimal notation.
   A network prefix that uses the Classless Inter-Domain Routing (CIDR) notation is required as part of the network string. A network port must not be present in the network string. 

An example network string is the following:

<b>192.168.100/24</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV6_ADDRESS"></a><a id="net_string_ipv6_address"></a><dl>
<dt><b>NET_STRING_IPV6_ADDRESS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv6 address using Internet standard hexadecimal encoding.
   An IPv6 scope ID may be present in the network string. A network port or prefix must not be present in the network string.  

An example network string is the following:

<b>21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A%2</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></a><a id="net_string_ipv6_address_no_scope"></a><dl>
<dt><b>NET_STRING_IPV6_ADDRESS_NO_SCOPE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv6 address using Internet standard hexadecimal encoding. An IPv6 scope ID must not be  present in the network string. A network port or prefix must not be present in the network string.  

An example network string is the following:

<b>21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV6_SERVICE"></a><a id="net_string_ipv6_service"></a><dl>
<dt><b>NET_STRING_IPV6_SERVICE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv6 service using Internet standard hexadecimal encoding.
   A network port is required as part of the network string. An IPv6 scope ID may be present in the network string. A prefix must not be present in the network string. 

An example network string with a scope ID is the following:

<b>[21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A%2]:8080</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></a><a id="net_string_ipv6_service_no_scope"></a><dl>
<dt><b>NET_STRING_IPV6_SERVICE_NO_SCOPE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv6 service using Internet standard hexadecimal encoding.
   A network port is required as part of the network string. An IPv6 scope ID must not be present in the network string. A prefix must not be present in the network string. 

An example network string is the following:

<b>21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A:8080</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IPV6_NETWORK"></a><a id="net_string_ipv6_network"></a><dl>
<dt><b>NET_STRING_IPV6_NETWORK</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv6 network using Internet standard hexadecimal encoding.
   A network prefix in CIDR notation is required as part of the network string. A network port or scope ID must not be present in the network string. 

An example network string is the following:

<b>21DA:D3::/48</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_NAMED_ADDRESS"></a><a id="net_string_named_address"></a><dl>
<dt><b>NET_STRING_NAMED_ADDRESS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an Internet address using a Domain Name System (DNS) name.
   A network port or prefix must not be present in the network string. 

An example network string is the following:

<b>www.microsoft.com</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_NAMED_SERVICE"></a><a id="net_string_named_service"></a><dl>
<dt><b>NET_STRING_NAMED_SERVICE</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an Internet service using a DNS name.
   A network port must be present in the network string. 

An example network string is the following:

<b>www.microsoft.com:80</b>

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IP_ADDRESS"></a><a id="net_string_ip_address"></a><dl>
<dt><b>NET_STRING_IP_ADDRESS</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 address using Internet standard dotted-decimal notation or an IPv6 address using the Internet standard hexadecimal encoding.
   An IPv6 scope ID may be present in the network string. A network port or prefix must not be present in the network string.  

This type matches either the <b>NET_STRING_IPV4_ADDRESS</b> or <b>NET_STRING_IPV6_ADDRESS</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IP_ADDRESS_NO_SCOPE"></a><a id="net_string_ip_address_no_scope"></a><dl>
<dt><b>NET_STRING_IP_ADDRESS_NO_SCOPE</b></dt>
<dt>0x00000011</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 address using Internet standard dotted-decimal notation or an IPv6 address using Internet standard hexadecimal encoding.
   An IPv6 scope ID must not be present in the network string. A network port or prefix must not be present in the network string.  

This type matches either the <b>NET_STRING_IPV4_ADDRESS</b> or <b>NET_STRING_IPV6_ADDRESS_NO_SCOPE</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IP_SERVICE"></a><a id="net_string_ip_service"></a><dl>
<dt><b>NET_STRING_IP_SERVICE</b></dt>
<dt>0x00000022</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 service or IPv6 service.
   A network port is required as part of the network string. An IPv6 scope ID may be present in the network string. A prefix must not be present in the network string. 

This type matches either the <b>NET_STRING_IPV4_SERVICE</b> or <b>NET_STRING_IPV6_SERVICE</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IP_SERVICE_NO_SCOPE"></a><a id="net_string_ip_service_no_scope"></a><dl>
<dt><b>NET_STRING_IP_SERVICE_NO_SCOPE</b></dt>
<dt>0x00000042</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 service or IPv6 service.
   A network port is required as part of the network string. An IPv6 scope ID must not be present in the network string. A prefix must not be present in the network string. 

This type matches either the <b>NET_STRING_IPV4_SERVICE</b> or <b>NET_STRING_IPV6_SERVICE_NO_SCOPE</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_IP_NETWORK"></a><a id="net_string_ip_network"></a><dl>
<dt><b>NET_STRING_IP_NETWORK</b></dt>
<dt>0x00000084</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 or IPv6 network.
   A network prefix in CIDR notation is required as part of the network string. A network port or scope ID must not be present in the network. 

This type matches either the <b>NET_STRING_IPV4_NETWORK</b> or <b>NET_STRING_IPV6_NETWORK</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_ANY_ADDRESS"></a><a id="net_string_any_address"></a><dl>
<dt><b>NET_STRING_ANY_ADDRESS</b></dt>
<dt>0x00000209</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 address in Internet standard dotted-decimal notation, an IPv6 address in Internet standard hexadecimal encoding, or a DNS name.
   An IPv6 scope ID may be present in the network string for an IPv6 address. A network port or prefix must not be present in the network string.  

This type matches either the <b>NET_STRING_NAMED_ADDRESS</b> or <b>NET_STRING_IP_ADDRESS</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></a><a id="net_string_any_address_no_scope"></a><dl>
<dt><b>NET_STRING_ANY_ADDRESS_NO_SCOPE</b></dt>
<dt>0x00000211</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 address in Internet standard dotted-decimal notation, an IPv6 address in Internet standard hexadecimal encoding, or a DNS name.
   An IPv6 scope ID must not be present in the network string for an IPv6 address. A network port or prefix must not be present in the network string.  

This type matches either the <b>NET_STRING_NAMED_ADDRESS</b> or <b>NET_STRING_IP_ADDRESS_NO_SCOPE</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_ANY_SERVICE"></a><a id="net_string_any_service"></a><dl>
<dt><b>NET_STRING_ANY_SERVICE</b></dt>
<dt>0x00000222</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 service or IPv6 service using IP address notation or a DNS name.
   A network port is required as part of the network string. An IPv6 scope ID may be present in the network string. A prefix must not be present in the network string. 

This type matches either the <b>NET_STRING_NAMED_SERVICE</b> or <b>NET_STRING_IP_SERVICE</b> types.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_STRING_ANY_SERVICE_NO_SCOPE"></a><a id="net_string_any_service_no_scope"></a><dl>
<dt><b>NET_STRING_ANY_SERVICE_NO_SCOPE</b></dt>
<dt>0x00000242</dt>
</dl>
</td>
<td width="60%">
The <i>NetworkString</i> parameter  points to an IPv4 service or IPv6 service using IP address notation or a DNS name.
   A network port is required as part of the network string. An IPv6 scope ID must not be present in the network string. A prefix must not be present in the network string. 

This type matches either the <b>NET_STRING_NAMED_SERVICE</b> or <b>NET_STRING_IP_SERVICE_NO_SCOPE</b> types.

</td>
</tr>
</table>

### -param AddressInfo [out, optional]

On success, the function returns a pointer to a <b>NET_ADDRESS_INFO</b> structure that contains the parsed IP address information if a <b>NULL</b> pointer was not passed in this parameter.

### -param PortNumber [out, optional]

On success, the function returns a pointer to the parsed network port in host order if a <b>NULL</b> pointer was not passed in this parameter. If a network port was not present in the <i>NetworkString</i> parameter, then a pointer to a value of zero is returned.

### -param PrefixLength [out, optional]

On success, the function returns a pointer to the parsed prefix length if a <b>NULL</b> pointer was not passed in this parameter. If a prefix was not present in the <i>NetworkString</i> parameter, then a pointer to a value of -1 is returned.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed to the function is too small. This error is returned if the buffer pointed to by the <i>AddressInfo</i> parameter is too small to hold the parsed 
    network address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>NetworkString</i> parameter

</td>
</tr>
</table>

## -remarks

The <b>ParseNetworkString</b> function parses the input network string passed in the <i>NetworkString</i> parameter and checks whether it
    is a legal representation of one of the string types as specified in 
    the <i>Types</i> argument. If the string matches a type and its specification,
    the function succeeds and can optionally return the parsed result
    to the caller in the optional <i>AddressInfo</i>, <i>PortNumber</i>, and <i>PrefixLength</i> parameters when these parameters are not <b>NULL</b> pointers.

The <b>ParseNetworkString</b> function can parse representations of IPv4 or IPv6 addresses, 
    services, and networks, as well as named Internet addresses and 
    services using DNS names.


The [NET_ADDRESS_INFO](/windows/desktop/api/iphlpapi/ns-iphlpapi-net_address_info) structure pointed to by the <i>AddressInfo</i> parameter. The SOCKADDR_IN and SOCKADDR structures are defined in the  <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. The SOCKADDR_IN6 structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included by the <i>Ws2tcpip.h</i> header file. In order to use the <b>ParseNetworkString</b> function  and the <b>NET_ADDRESS_INFO</b> structure, the <i>Winsock2.h</i> and <i>Ws2tcpip.h</i> header files must be included before the <i>Iphlpapi.h</i> header file.

## -see-also

[NET_ADDRESS_FORMAT](/windows/desktop/api/iphlpapi/ne-iphlpapi-net_address_format)



[NET_ADDRESS_INFO](/windows/desktop/api/iphlpapi/ns-iphlpapi-net_address_info)



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



SOCKADDR_IN



SOCKADDR_IN6