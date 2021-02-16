---
UID: NS:ipexport.icmpv6_echo_reply_lh
title: ICMPV6_ECHO_REPLY_LH (ipexport.h)
description: Describes the data returned in response to an IPv6 echo request.
helpviewer_keywords: ["*PICMPV6_ECHO_REPLY","*PICMPV6_ECHO_REPLY_LH","ICMPV6_ECHO_REPLY","ICMPV6_ECHO_REPLY structure [IP Helper]","ICMPV6_ECHO_REPLY_LH","IP_BAD_DESTINATION","IP_BAD_HEADER","IP_BAD_OPTION","IP_BAD_REQ","IP_BAD_ROUTE","IP_BUF_TOO_SMALL","IP_DEST_HOST_UNREACHABLE","IP_DEST_NET_UNREACHABLE","IP_DEST_PORT_UNREACHABLE","IP_DEST_PROT_UNREACHABLE","IP_DEST_SCOPE_MISMATCH","IP_DEST_UNREACHABLE","IP_GENERAL_FAILURE","IP_HW_ERROR","IP_ICMP_ERROR","IP_NO_RESOURCES","IP_OPTION_TOO_BIG","IP_PACKET_TOO_BIG","IP_PARAM_PROBLEM","IP_REQ_TIMED_OUT","IP_SOURCE_QUENCH","IP_SUCCESS","IP_TIME_EXCEEDED","IP_TTL_EXPIRED_REASSEM","IP_TTL_EXPIRED_TRANSIT","IP_UNRECOGNIZED_NEXT_HEADER","PICMPV6_ECHO_REPLY","PICMPV6_ECHO_REPLY structure pointer [IP Helper]","ipexport/ICMPV6_ECHO_REPLY","ipexport/PICMPV6_ECHO_REPLY","iphlp.icmpv6_echo_reply"]
old-location: iphlp\icmpv6_echo_reply.htm
tech.root: IpHlp
ms.assetid: 8ea4ce42-6164-4b8e-9e79-524f456c8d09
ms.date: 12/05/2018
ms.keywords: '*PICMPV6_ECHO_REPLY, *PICMPV6_ECHO_REPLY_LH, ICMPV6_ECHO_REPLY, ICMPV6_ECHO_REPLY structure [IP Helper], ICMPV6_ECHO_REPLY_LH, IP_BAD_DESTINATION, IP_BAD_HEADER, IP_BAD_OPTION, IP_BAD_REQ, IP_BAD_ROUTE, IP_BUF_TOO_SMALL, IP_DEST_HOST_UNREACHABLE, IP_DEST_NET_UNREACHABLE, IP_DEST_PORT_UNREACHABLE, IP_DEST_PROT_UNREACHABLE, IP_DEST_SCOPE_MISMATCH, IP_DEST_UNREACHABLE, IP_GENERAL_FAILURE, IP_HW_ERROR, IP_ICMP_ERROR, IP_NO_RESOURCES, IP_OPTION_TOO_BIG, IP_PACKET_TOO_BIG, IP_PARAM_PROBLEM, IP_REQ_TIMED_OUT, IP_SOURCE_QUENCH, IP_SUCCESS, IP_TIME_EXCEEDED, IP_TTL_EXPIRED_REASSEM, IP_TTL_EXPIRED_TRANSIT, IP_UNRECOGNIZED_NEXT_HEADER, PICMPV6_ECHO_REPLY, PICMPV6_ECHO_REPLY structure pointer [IP Helper], ipexport/ICMPV6_ECHO_REPLY, ipexport/PICMPV6_ECHO_REPLY, iphlp.icmpv6_echo_reply'
req.header: ipexport.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: ICMPV6_ECHO_REPLY_LH, *PICMPV6_ECHO_REPLY_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - icmpv6_echo_reply_lh
 - ipexport/icmpv6_echo_reply_lh
 - PICMPV6_ECHO_REPLY_LH
 - ipexport/PICMPV6_ECHO_REPLY_LH
 - ICMPV6_ECHO_REPLY_LH
 - ipexport/ICMPV6_ECHO_REPLY_LH
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
 - ICMPV6_ECHO_REPLY
---

# ICMPV6_ECHO_REPLY_LH structure


## -description

The 
<b>ICMPV6_ECHO_REPLY</b> structure describes the data returned in response to an IPv6 echo request.

## -struct-fields

### -field Address

Type: <b>IPV6_ADDRESS_EX</b>

The replying IPv6 address, in the form of an <a href="/windows/desktop/api/ipexport/ns-ipexport-ipv6_address_ex">IPV6_ADDRESS_EX</a> structure.

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
The destination network was unreachable. In IPv6 terminology, this status value is also defined as <b>IP_DEST_NO_ROUTE</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_HOST_UNREACHABLE"></a><a id="ip_dest_host_unreachable"></a><dl>
<dt><b>IP_DEST_HOST_UNREACHABLE</b></dt>
<dt>11003</dt>
</dl>
</td>
<td width="60%">
The destination host was unreachable. In IPv6 terminology, this status value is also defined as <b>IP_DEST_ADDR_UNREACHABLE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_PROT_UNREACHABLE"></a><a id="ip_dest_prot_unreachable"></a><dl>
<dt><b>IP_DEST_PROT_UNREACHABLE</b></dt>
<dt>11004</dt>
</dl>
</td>
<td width="60%">
The destination protocol was unreachable. In IPv6 terminology, this status value is also defined as <b>IP_DEST_PROHIBITED</b>.

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
The hop limit for IPv6 expired in transit. In IPv6 terminology, this status value is also defined as <b>IP_HOP_LIMIT_EXCEEDED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_TTL_EXPIRED_REASSEM"></a><a id="ip_ttl_expired_reassem"></a><dl>
<dt><b>IP_TTL_EXPIRED_REASSEM</b></dt>
<dt>11014</dt>
</dl>
</td>
<td width="60%">
The hop limit for IPv6 expired during fragment reassembly. In IPv6 terminology, this status value is also defined as <b>IP_REASSEMBLY_TIME_EXCEEDED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_PARAM_PROBLEM"></a><a id="ip_param_problem"></a><dl>
<dt><b>IP_PARAM_PROBLEM</b></dt>
<dt>11015</dt>
</dl>
</td>
<td width="60%">
A parameter problem. In IPv6 terminology, this status value is also defined as <b>IP_PARAMETER_PROBLEM</b>.

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
<td width="40%"><a id="IP_DEST_UNREACHABLE"></a><a id="ip_dest_unreachable"></a><dl>
<dt><b>IP_DEST_UNREACHABLE</b></dt>
<dt>11040</dt>
</dl>
</td>
<td width="60%">
The destination was unreachable. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_TIME_EXCEEDED"></a><a id="ip_time_exceeded"></a><dl>
<dt><b>IP_TIME_EXCEEDED</b></dt>
<dt>11041</dt>
</dl>
</td>
<td width="60%">
The time was exceeded. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_BAD_HEADER"></a><a id="ip_bad_header"></a><dl>
<dt><b>IP_BAD_HEADER</b></dt>
<dt>11042</dt>
</dl>
</td>
<td width="60%">
A bad IP header was encountered. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_UNRECOGNIZED_NEXT_HEADER"></a><a id="ip_unrecognized_next_header"></a><dl>
<dt><b>IP_UNRECOGNIZED_NEXT_HEADER</b></dt>
<dt>11043</dt>
</dl>
</td>
<td width="60%">
An unrecognized next header was encountered. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ICMP_ERROR"></a><a id="ip_icmp_error"></a><dl>
<dt><b>IP_ICMP_ERROR</b></dt>
<dt>11044</dt>
</dl>
</td>
<td width="60%">
An ICMP error occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_DEST_SCOPE_MISMATCH"></a><a id="ip_dest_scope_mismatch"></a><dl>
<dt><b>IP_DEST_SCOPE_MISMATCH</b></dt>
<dt>11045</dt>
</dl>
</td>
<td width="60%">
A destination scope ID mismatch occurred. 

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

Type: <b>unsigned int</b>

The round trip time, in milliseconds.

## -remarks

The <b>ICMPV6_ECHO_REPLY</b> structure is used by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> function to return the response to an IPv6 echo request. The reply data that contains the message body from the ICMPV6 response follows the <b>ICMPV6_ECHO_REPLY</b> structure in memory.


For IPv6, some of the possible values for the <b>Status</b> member are specified in 
RFC 2163. For more information, see <a href="http://tools.ietf.org/html/rfc2463">www.ietf.org/rfc/rfc2463.txt</a>.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiperrorstring">GetIpErrorString</a> function can be used to retrieve the IP helper error string for the <b>IP_STATUS</b> error code in the <b>Status</b> member.

The <b>ICMPV6_ECHO_REPLY</b> structure is defined in public header files included in the Microsoft Windows Software Development Kit (SDK), but this structure is used by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> function on Windows XP and later.  

In the Windows SDK, the <b>ICMPV6_ECHO_REPLY_LH</b> structure is defined  when compiling an 
     application if the target platform is Windows XP and later 
     (<code>NTDDI_VERSION &gt;= NTDDI_XP</code>, 
     <code>_WIN32_WINNT &gt;= 0x0501</code>, or 
     <code>WINVER &gt;= 0x0501</code>). The <b>ICMPV6_ECHO_REPLY_LH</b> structure is typedefed to the <b>ICMPV6_ECHO_REPLY</b> structure. When compiling an application if the target 
     platform is not Windows XP and later, the 
     <b>ICMPV6_ECHO_REPLY</b> structure is undefined.

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiperrorstring">GetIpErrorString</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ipv6_address_ex">IPV6_ADDRESS_EX</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>