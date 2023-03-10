---
UID: NF:icmpapi.IcmpParseReplies
title: IcmpParseReplies function (icmpapi.h)
description: Parses the reply buffer provided and returns the number of ICMP echo request responses found.
helpviewer_keywords: ["IcmpParseReplies","IcmpParseReplies function [IP Helper]","_iphlp_icmpparsereplies","icmpapi/IcmpParseReplies","iphlp.icmpparsereplies"]
old-location: iphlp\icmpparsereplies.htm
tech.root: IpHlp
ms.assetid: ec7c2a5f-5406-4350-b795-6e72fe25f62d
ms.date: 12/05/2018
ms.keywords: IcmpParseReplies, IcmpParseReplies function [IP Helper], _iphlp_icmpparsereplies, icmpapi/IcmpParseReplies, iphlp.icmpparsereplies
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Iphlpapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP; Icmp.dll on Windows 2000 Server and Windows 2000 Professional
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IcmpParseReplies
 - icmpapi/IcmpParseReplies
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
 - Icmp.dll
api_name:
 - IcmpParseReplies
---

# IcmpParseReplies function


## -description

The 
<b>IcmpParseReplies</b> function parses the reply buffer provided and returns the number of ICMP echo request responses found.

## -parameters

### -param ReplyBuffer [in]

The buffer passed to 
<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>. This is rewritten to hold an array of 
<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a> structures, its type is <b>PICMP_ECHO_REPLY</b>. 

On a 64-bit platform, this buffer is rewritten to hold an array of <a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a> structures, its type is <b>PICMP_ECHO_REPLY32</b>.

### -param ReplySize [in]

The size, in bytes, of the buffer pointed to by the <i>ReplyBuffer</i> parameter.

## -returns

The 
<b>IcmpParseReplies</b> function returns the number of ICMP responses found on success. The function returns zero on error. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for additional error information.

## -remarks

The <b>IcmpParseReplies</b> function should not be used on a reply buffer previously passed to 
<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>. The 
<b>IcmpSendEcho</b> function parses that buffer before returning to the user. Use this function only with 
<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>.

The <b>IcmpParseReplies</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpParseReplies</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpParseReplies</b> in the <i>Iphlpapi.dll</i> with calls to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpParseReplies</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply32">ICMP_ECHO_REPLY32</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<b>IcmpSendEcho</b>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>