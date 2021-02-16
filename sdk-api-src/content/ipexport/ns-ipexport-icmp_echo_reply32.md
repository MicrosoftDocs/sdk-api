---
UID: NS:ipexport.icmp_echo_reply32
title: ICMP_ECHO_REPLY32 (ipexport.h)
description: Describes the data returned in response to an IPv4 echo request on a 64-bit platform.
helpviewer_keywords: ["*PICMP_ECHO_REPLY32","ICMP_ECHO_REPLY32","ICMP_ECHO_REPLY32 structure [IP Helper]","IP_BAD_DESTINATION","IP_BAD_OPTION","IP_BAD_REQ","IP_BAD_ROUTE","IP_BUF_TOO_SMALL","IP_DEST_HOST_UNREACHABLE","IP_DEST_NET_UNREACHABLE","IP_DEST_PORT_UNREACHABLE","IP_DEST_PROT_UNREACHABLE","IP_GENERAL_FAILURE","IP_HW_ERROR","IP_NO_RESOURCES","IP_OPTION_TOO_BIG","IP_PACKET_TOO_BIG","IP_PARAM_PROBLEM","IP_REQ_TIMED_OUT","IP_SOURCE_QUENCH","IP_SUCCESS","IP_TTL_EXPIRED_REASSEM","IP_TTL_EXPIRED_TRANSIT","PICMP_ECHO_REPLY32","PICMP_ECHO_REPLY32 structure pointer [IP Helper]","ipexport/ICMP_ECHO_REPLY32","ipexport/PICMP_ECHO_REPLY32","iphlp.icmp_echo_reply32"]
old-location: iphlp\icmp_echo_reply32.htm
tech.root: IpHlp
ms.assetid: 4a84f29c-31bd-453c-b215-300cc782595f
ms.date: 12/05/2018
ms.keywords: '*PICMP_ECHO_REPLY32, ICMP_ECHO_REPLY32, ICMP_ECHO_REPLY32 structure [IP Helper], IP_BAD_DESTINATION, IP_BAD_OPTION, IP_BAD_REQ, IP_BAD_ROUTE, IP_BUF_TOO_SMALL, IP_DEST_HOST_UNREACHABLE, IP_DEST_NET_UNREACHABLE, IP_DEST_PORT_UNREACHABLE, IP_DEST_PROT_UNREACHABLE, IP_GENERAL_FAILURE, IP_HW_ERROR, IP_NO_RESOURCES, IP_OPTION_TOO_BIG, IP_PACKET_TOO_BIG, IP_PARAM_PROBLEM, IP_REQ_TIMED_OUT, IP_SOURCE_QUENCH, IP_SUCCESS, IP_TTL_EXPIRED_REASSEM, IP_TTL_EXPIRED_TRANSIT, PICMP_ECHO_REPLY32, PICMP_ECHO_REPLY32 structure pointer [IP Helper], ipexport/ICMP_ECHO_REPLY32, ipexport/PICMP_ECHO_REPLY32, iphlp.icmp_echo_reply32'
req.header: ipexport.h
req.include-header: Iphlpapi.h
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
req.typenames: ICMP_ECHO_REPLY32, *PICMP_ECHO_REPLY32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - icmp_echo_reply32
 - ipexport/icmp_echo_reply32
 - PICMP_ECHO_REPLY32
 - ipexport/PICMP_ECHO_REPLY32
 - ICMP_ECHO_REPLY32
 - ipexport/ICMP_ECHO_REPLY32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipexport.h
api_name:
 - ICMP_ECHO_REPLY32
---

# ICMP_ECHO_REPLY32 structure


## -description

The 
<b>ICMP_ECHO_REPLY32</b> structure describes the data returned in response to an IPv4 echo request on a 64-bit platform.

## -struct-fields

### -field Address

Type: <b>IPAddr</b>

The replying IPv4 address, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

### -field Status

Type: <b>ULONG</b>

The status of the echo request, in the form of an <b>IP_STATUS</b> code. The possible values for this member are defined in the <i>Ipexport.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IP_SUCCESS"></a><a id="ip_success"></a><dl>
<dt><b>IP_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The status was success.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BUF_TOO_SMALL"></a><a id="ip_buf_too_small"></a><dl>
<dt><b>IP_BUF_TOO_SMALL</b></dt>
<dt>11001</dt>
</dl>
</td>
<td width="60%">
The reply buffer was too small.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_NET_UNREACHABLE"></a><a id="ip_dest_net_unreachable"></a><dl>
<dt><b>IP_DEST_NET_UNREACHABLE</b></dt>
<dt>11002</dt>
</dl>
</td>
<td width="60%">
The destination network was unreachable. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_HOST_UNREACHABLE"></a><a id="ip_dest_host_unreachable"></a><dl>
<dt><b>IP_DEST_HOST_UNREACHABLE</b></dt>
<dt>11003</dt>
</dl>
</td>
<td width="60%">
The destination host was unreachable. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_PROT_UNREACHABLE"></a><a id="ip_dest_prot_unreachable"></a><dl>
<dt><b>IP_DEST_PROT_UNREACHABLE</b></dt>
<dt>11004</dt>
</dl>
</td>
<td width="60%">
The destination protocol was unreachable. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_PORT_UNREACHABLE"></a><a id="ip_dest_port_unreachable"></a><dl>
<dt><b>IP_DEST_PORT_UNREACHABLE</b></dt>
<dt>11005</dt>
</dl>
</td>
<td width="60%">
The destination port was unreachable. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_NO_RESOURCES"></a><a id="ip_no_resources"></a><dl>
<dt><b>IP_NO_RESOURCES</b></dt>
<dt>11006</dt>
</dl>
</td>
<td width="60%">
Insufficient IP resources were available.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BAD_OPTION_"></a><a id="ip_bad_option_"></a><dl>
<dt><b>IP_BAD_OPTION </b></dt>
<dt>11007</dt>
</dl>
</td>
<td width="60%">
A bad IP option was specified.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_HW_ERROR"></a><a id="ip_hw_error"></a><dl>
<dt><b>IP_HW_ERROR</b></dt>
<dt>11008</dt>
</dl>
</td>
<td width="60%">
A hardware error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_PACKET_TOO_BIG"></a><a id="ip_packet_too_big"></a><dl>
<dt><b>IP_PACKET_TOO_BIG</b></dt>
<dt>11009</dt>
</dl>
</td>
<td width="60%">
The packet was too big.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_REQ_TIMED_OUT"></a><a id="ip_req_timed_out"></a><dl>
<dt><b>IP_REQ_TIMED_OUT</b></dt>
<dt>11010</dt>
</dl>
</td>
<td width="60%">
The request timed out.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BAD_REQ"></a><a id="ip_bad_req"></a><dl>
<dt><b>IP_BAD_REQ</b></dt>
<dt>11011</dt>
</dl>
</td>
<td width="60%">
A bad request.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BAD_ROUTE"></a><a id="ip_bad_route"></a><dl>
<dt><b>IP_BAD_ROUTE</b></dt>
<dt>11012</dt>
</dl>
</td>
<td width="60%">
A bad route.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_TTL_EXPIRED_TRANSIT"></a><a id="ip_ttl_expired_transit"></a><dl>
<dt><b>IP_TTL_EXPIRED_TRANSIT</b></dt>
<dt>11013</dt>
</dl>
</td>
<td width="60%">
The time to live (TTL) expired in transit. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_TTL_EXPIRED_REASSEM"></a><a id="ip_ttl_expired_reassem"></a><dl>
<dt><b>IP_TTL_EXPIRED_REASSEM</b></dt>
<dt>11014</dt>
</dl>
</td>
<td width="60%">
The time to live expired during fragment reassembly. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_PARAM_PROBLEM"></a><a id="ip_param_problem"></a><dl>
<dt><b>IP_PARAM_PROBLEM</b></dt>
<dt>11015</dt>
</dl>
</td>
<td width="60%">
A parameter problem. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_SOURCE_QUENCH"></a><a id="ip_source_quench"></a><dl>
<dt><b>IP_SOURCE_QUENCH</b></dt>
<dt>11016</dt>
</dl>
</td>
<td width="60%">
Datagrams are arriving too fast to be processed and datagrams may have been discarded. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_OPTION_TOO_BIG"></a><a id="ip_option_too_big"></a><dl>
<dt><b>IP_OPTION_TOO_BIG</b></dt>
<dt>11017</dt>
</dl>
</td>
<td width="60%">
An IP option was too big. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BAD_DESTINATION"></a><a id="ip_bad_destination"></a><dl>
<dt><b>IP_BAD_DESTINATION</b></dt>
<dt>11018</dt>
</dl>
</td>
<td width="60%">
A bad destination. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_GENERAL_FAILURE"></a><a id="ip_general_failure"></a><dl>
<dt><b>IP_GENERAL_FAILURE</b></dt>
<dt>11050</dt>
</dl>
</td>
<td width="60%">
A general failure. This error can be returned for some malformed ICMP packets. 

</td>
</tr>
</table>

### -field RoundTripTime

Type: <b>ULONG</b>

The round trip time, in milliseconds.

### -field DataSize

Type: <b>USHORT</b>

The data size, in bytes, of the reply.

### -field Reserved

Type: <b>USHORT</b>

Reserved for system use.

### -field Data

Type: <b>VOID * POINTER_32</b>

A pointer to the reply data.

### -field Options

Type: <b>struct ip_option_information32</b>

The IP options in the IP header of the reply, in the form of an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a> structure.

## -remarks

The <b>ICMP_ECHO_REPLY32</b> structure is used by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> function to return the response to an IPv4 echo request on a 64-bit platform. This structure is only defined if _WIN64 is defined.

For IPv4, some of the possible values for the <b>Status</b> member are specified in 
<a href="https://www.ietf.org/rfc/rfc792.txt">RFC 792</a>.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiperrorstring">GetIpErrorString</a> function can be used to retrieve the IP helper error string for the <b>IP_STATUS</b> error code in the <b>Status</b> member.

The <b>ICMP_ECHO_REPLY32</b> structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiperrorstring">GetIpErrorString</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information32">IP_OPTION_INFORMATION32</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>