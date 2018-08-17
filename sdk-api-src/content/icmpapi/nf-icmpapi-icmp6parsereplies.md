---
UID: NF:icmpapi.Icmp6ParseReplies
title: Icmp6ParseReplies function
author: windows-sdk-content
description: The Icmp6ParseReplies function parses the reply buffer provided and returns an IPv6 ICMPv6 echo response reply if found.
old-location: iphlp\icmp6parsereplies.htm
old-project: iphlp
ms.assetid: b4d63ffd-37ad-4901-b017-205fb15381e7
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: Icmp6ParseReplies, Icmp6ParseReplies function [IP Helper], icmpapi/Icmp6ParseReplies, iphlp.icmp6parsereplies
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: icmpapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - Icmp6ParseReplies
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# Icmp6ParseReplies function


## -description


The <b>Icmp6ParseReplies</b> function parses the reply buffer provided and returns an IPv6 ICMPv6 echo response reply if found.


## -parameters




### -param ReplyBuffer [in]

A pointer to the buffer passed to 
the <a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a> function. This parameter is points to an <a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structure to hold the response.


### -param ReplySize [in]

The size, in bytes, of the buffer pointed to by the <i>ReplyBuffer</i> parameter.


## -returns



The <b>Icmp6ParseReplies</b> function returns 1 on success. In this case, the <b>Status</b> member in the <a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structure pointed to by the <i>ReplyBuffer</i> parameter will be either <b>IP_SUCCESS</b> if the target node responded or <b>IP_TTL_EXPIRED_TRANSIT</b>.

If the return value is zero, extended error information is available through 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
						

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>Icmp6ParseReplies</b> function is used by IPv6 to parse replies that result from an ICMPv6 echo request. The <b>Icmp6ParseReplies</b> function  parses a reply buffer previously passed to 
the <a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a> function. Use the <b>Icmp6ParseReplies</b>  function only with 
the <b>Icmp6SendEcho2</b> function.

The <b>Icmp6ParseReplies</b> function cannot be used on a reply buffer previously passed to 
<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a> or <a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a> for IPv4.

For IPv4, use the <a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>,  <b>IcmpSendEcho</b>, <a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>, <a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>, and <a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.




## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/ce8f11bb-1e33-41bd-adb9-c18efadd4d0b">IcmpCloseHandle</a>



<a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>



<a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>
 

 

