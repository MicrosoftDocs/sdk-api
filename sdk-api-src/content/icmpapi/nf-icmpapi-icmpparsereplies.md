---
UID: NF:icmpapi.IcmpParseReplies
title: IcmpParseReplies function (icmpapi.h)
author: windows-sdk-content
description: Parses the reply buffer provided and returns the number of ICMP echo request responses found.
old-location: iphlp\icmpparsereplies.htm
tech.root: IpHlp
ms.assetid: ec7c2a5f-5406-4350-b795-6e72fe25f62d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IcmpParseReplies, IcmpParseReplies function [IP Helper], _iphlp_icmpparsereplies, icmpapi/IcmpParseReplies, iphlp.icmpparsereplies
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IcmpParseReplies function


## -description


The 
<b>IcmpParseReplies</b> function parses the reply buffer provided and returns the number of ICMP echo request responses found.


## -parameters




### -param ReplyBuffer [in]

The buffer passed to 
<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>. This is rewritten to hold an array of 
<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a> structures, its type is <b>PICMP_ECHO_REPLY</b>. 

On a 64-bit plaform, this buffer is rewritten to hold an array of <a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a> structures, its type is <b>PICMP_ECHO_REPLY32</b>.


### -param ReplySize [in]

The size, in bytes, of the buffer pointed to by the <i>ReplyBuffer</i> parameter.


## -returns



The 
<b>IcmpParseReplies</b> function returns the number of ICMP responses found on success. The function returns zero on error. Call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional error information.




## -remarks



The <b>IcmpParseReplies</b> function should not be used on a reply buffer previously passed to 
<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a>. The 
<b>IcmpSendEcho</b> function parses that buffer before returning to the user. Use this function only with 
<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>.

The <b>IcmpParseReplies</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpParseReplies</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpParseReplies</b> in the <i>Iphlpapi.dll</i> with calls to <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpParseReplies</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.




## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/ce8f11bb-1e33-41bd-adb9-c18efadd4d0b">IcmpCloseHandle</a>



<a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>



<b>IcmpSendEcho</b>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>
 

 

