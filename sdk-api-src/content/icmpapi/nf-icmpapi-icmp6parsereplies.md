---
UID: NF:icmpapi.Icmp6ParseReplies
title: Icmp6ParseReplies function (icmpapi.h)
description: The Icmp6ParseReplies function parses the reply buffer provided and returns an IPv6 ICMPv6 echo response reply if found.
helpviewer_keywords: ["Icmp6ParseReplies","Icmp6ParseReplies function [IP Helper]","icmpapi/Icmp6ParseReplies","iphlp.icmp6parsereplies"]
old-location: iphlp\icmp6parsereplies.htm
tech.root: IpHlp
ms.assetid: b4d63ffd-37ad-4901-b017-205fb15381e7
ms.date: 12/05/2018
ms.keywords: Icmp6ParseReplies, Icmp6ParseReplies function [IP Helper], icmpapi/Icmp6ParseReplies, iphlp.icmp6parsereplies
req.header: icmpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Icmp6ParseReplies
 - icmpapi/Icmp6ParseReplies
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
 - Icmp6ParseReplies
---

# Icmp6ParseReplies function


## -description

The <b>Icmp6ParseReplies</b> function parses the reply buffer provided and returns an IPv6 ICMPv6 echo response reply if found.

## -parameters

### -param ReplyBuffer [in]

A pointer to the buffer passed to 
the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a> function. This parameter is points to an <a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a> structure to hold the response.

### -param ReplySize [in]

The size, in bytes, of the buffer pointed to by the <i>ReplyBuffer</i> parameter.

## -returns

The <b>Icmp6ParseReplies</b> function returns 1 on success. In this case, the <b>Status</b> member in the <a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a> structure pointed to by the <i>ReplyBuffer</i> parameter will be either <b>IP_SUCCESS</b> if the target node responded or <b>IP_TTL_EXPIRED_TRANSIT</b>.

If the return value is zero, extended error information is available through 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
						

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A general failure occurred. This error is returned if the <i>ReplyBuffer</i> parameter is a <b>NULL</b> pointer or the <i>ReplySize </i> parameter is zero. 

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>Icmp6ParseReplies</b> function is used by IPv6 to parse replies that result from an ICMPv6 echo request. The <b>Icmp6ParseReplies</b> function  parses a reply buffer previously passed to 
the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a> function. Use the <b>Icmp6ParseReplies</b>  function only with 
the <b>Icmp6SendEcho2</b> function.

The <b>Icmp6ParseReplies</b> function cannot be used on a reply buffer previously passed to 
<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a> or <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a> for IPv4.

For IPv4, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>,  <b>IcmpSendEcho</b>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>