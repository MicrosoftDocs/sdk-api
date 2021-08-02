---
UID: NF:iphlpapi.GetIpErrorString
title: GetIpErrorString function (iphlpapi.h)
description: The GetIpErrorString function retrieves an IP Helper error string.
helpviewer_keywords: ["GetIpErrorString","GetIpErrorString function [IP Helper]","iphlp.getiperrorstring","iphlpapi/GetIpErrorString"]
old-location: iphlp\getiperrorstring.htm
tech.root: IpHlp
ms.assetid: 4f71777a-2e87-4411-89fd-12c165d4d8ae
ms.date: 12/05/2018
ms.keywords: GetIpErrorString, GetIpErrorString function [IP Helper], iphlp.getiperrorstring, iphlpapi/GetIpErrorString
req.header: iphlpapi.h
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
 - GetIpErrorString
 - iphlpapi/GetIpErrorString
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
 - GetIpErrorString
---

# GetIpErrorString function


## -description

The <b>GetIpErrorString</b> function retrieves an IP Helper error string.

## -parameters

### -param ErrorCode [in]

The error code to be retrieved. The possible values for this parameter are defined in the <i>Ipexport.h</i> header file.

### -param Buffer [out]

A pointer to the buffer that contains the error code string if the function returns with NO_ERROR.

### -param Size [in, out]

A pointer to a <b>DWORD</b> that specifies the length, in characters, of the buffer pointed to by <i>Buffer</i> parameter, excluding the terminating null (i.e. the size of Buffer in characters, minus one).

## -returns

Returns NO_ERROR upon success.

If the function fails, use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -remarks

The <b>GetIpErrorString</b> function can be used to retrieve an IP Helper error string for an IP error code. The <b>IP_STATUS</b> error code passed in the <i>ErrorCode</i> parameter is returned in the <b>Status</b> member of the <a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>, <a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a>, and  <a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a> structures used by the ICMP and ICMPv6 functions.   The functions that use these structures include <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>, 
			<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>.

The syntax for the <b>GetIpErrorString</b> function was slightly changed on the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later. The data type for the <i>Buffer</i> parameter was changed from <b>PWCHAR</b> to <b>PWSTR</b>.

## -see-also

<a href="/windows/desktop/api/ipexport/ns-ipexport-icmpv6_echo_reply_lh">ICMPV6_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>