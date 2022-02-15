---
UID: NS:ipexport.ip_option_information32
title: IP_OPTION_INFORMATION32 (ipexport.h)
description: Describes the options to be included in the header of an IP packet on a 64-bit platform.
helpviewer_keywords: ["*PIP_OPTION_INFORMATION32","IP_FLAG_DF","IP_FLAG_REVERSE","IP_OPTION_INFORMATION32","IP_OPTION_INFORMATION32 structure [IP Helper]","PIP_OPTION_INFORMATION32","PIP_OPTION_INFORMATION32 structure pointer [IP Helper]","ipexport/IP_OPTION_INFORMATION32","ipexport/PIP_OPTION_INFORMATION32","iphlp.ip_option_information32"]
old-location: iphlp\ip_option_information32.htm
tech.root: IpHlp
ms.assetid: 3924230d-ff10-43ac-981c-81273bce6896
ms.date: 12/05/2018
ms.keywords: '*PIP_OPTION_INFORMATION32, IP_FLAG_DF, IP_FLAG_REVERSE, IP_OPTION_INFORMATION32, IP_OPTION_INFORMATION32 structure [IP Helper], PIP_OPTION_INFORMATION32, PIP_OPTION_INFORMATION32 structure pointer [IP Helper], ipexport/IP_OPTION_INFORMATION32, ipexport/PIP_OPTION_INFORMATION32, iphlp.ip_option_information32'
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
req.typenames: IP_OPTION_INFORMATION32, *PIP_OPTION_INFORMATION32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ip_option_information32
 - ipexport/ip_option_information32
 - PIP_OPTION_INFORMATION32
 - ipexport/PIP_OPTION_INFORMATION32
 - IP_OPTION_INFORMATION32
 - ipexport/IP_OPTION_INFORMATION32
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
 - IP_OPTION_INFORMATION32
---

# IP_OPTION_INFORMATION32 structure


## -description

The 
<b>IP_OPTION_INFORMATION32</b> structure describes the options to be included in the header of an IP packet on a 64-bit platform.

## -struct-fields

### -field Ttl

Type: <b>UCHAR</b>

The Time to Live field in an IPv4 packet header. This is the Hop Limit field in an IPv6 header.

### -field Tos

Type: <b>UCHAR</b>

The type of service field in an IPv4 header. This member is currently silently ignored.

### -field Flags

Type: <b>UCHAR</b>

The Flags field. In IPv4, this is the Flags field in the IPv4 header. In IPv6, this field is represented by  options headers.


For IPv4, the possible values for the <b>Flags</b> member are a combination of the following values defined in the <i>Ipexport.h</i> header file:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IP_FLAG_REVERSE"></a><a id="ip_flag_reverse"></a><dl>
<dt><b>IP_FLAG_REVERSE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
This value causes the IP packet to add in an IP routing header with
                   the source. This value is only applicable on Windows Vista and later. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_FLAG_DF"></a><a id="ip_flag_df"></a><dl>
<dt><b>IP_FLAG_DF</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
This value indicates that the packet should not be fragmented.

</td>
</tr>
</table>

### -field OptionsSize

Type: <b>UCHAR</b>

The size, in bytes, of IP options data.

### -field OptionsData

Type: <b>UCHAR * POINTER_32</b>

A pointer to options data.

## -remarks

The <b>IP_OPTION_INFORMATION32</b> structure is used to describe the options to be included in the header of an IP packet on a 64-bit platform. The  <b>IP_OPTION_INFORMATION32</b> structure is only defined if _WIN64 is defined.

The values in the <b>TTL</b>, <b>TOS</b> and <b>Flags</b>  members are carried in specific fields in the IP header.

The bytes in the <b>OptionsData</b>  member are carried in the options area that follows the standard IP header. 

With the exception of source route options for IPv4, the options data must be in the format to be transmitted on the wire as specified in 
<a href="https://www.ietf.org/rfc/rfc791.txt">RFC 791</a>. An IPv4 source route option should contain the full route, first hop through final destination, in the route data. The first hop is pulled out of the data and the option is reformatted accordingly. Otherwise, the route option should be formatted as specified in 
<a href="https://www.ietf.org/rfc/rfc791.txt">RFC 791</a>.

For use with IPv6, the options data must be in the format to be transmitted on the wire as specified in 
<a href="https://www.ietf.org/rfc/rfc2460.txt">RFC 2460</a>.

The <b>IP_OPTION_INFORMATION32</b> structure is a member of the <a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a> structure used by the by the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a> functions.

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_option_information">IP_OPTION_INFORMATION</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>