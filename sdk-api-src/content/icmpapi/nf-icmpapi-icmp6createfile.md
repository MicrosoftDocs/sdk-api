---
UID: NF:icmpapi.Icmp6CreateFile
title: Icmp6CreateFile function (icmpapi.h)
description: The Icmp6CreateFile function opens a handle on which IPv6 ICMP echo requests can be issued.
helpviewer_keywords: ["Icmp6CreateFile","Icmp6CreateFile function [IP Helper]","icmpapi/Icmp6CreateFile","iphlp.icmp6createfile"]
old-location: iphlp\icmp6createfile.htm
tech.root: IpHlp
ms.assetid: 2ddb23d8-a4e6-47c4-a552-2815ccaf055f
ms.date: 12/05/2018
ms.keywords: Icmp6CreateFile, Icmp6CreateFile function [IP Helper], icmpapi/Icmp6CreateFile, iphlp.icmp6createfile
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Icmp6CreateFile
 - icmpapi/Icmp6CreateFile
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
 - Icmp6CreateFile
---

# Icmp6CreateFile function


## -description

The 
<b>Icmp6CreateFile</b> function opens a handle on which IPv6 ICMP echo requests can be issued.



## -returns

The 
<b>Icmp6CreateFile</b> function returns an open handle on success. On failure, the function returns <b>INVALID_HANDLE_VALUE</b>. Call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for extended error information.

## -remarks

The 
<b>Icmp6CreateFile</b> function opens a handle on which IPv6 ICMP echo requests can be issued. The <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a> function is used to send the IPv6 ICMP echo requests. The <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> function is used to parse the IPv6 ICMP replies. The <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a> function is used to close the ICMP handle opened by the <b>Icmp6CreateFile</b> function. 

For IPv4, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a> function.

For IPv4, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>,  <b>IcmpSendEcho</b>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example opens a handle on which IPv6 ICMP echo requests can be issued. 


```cpp
#include <windows.h>
#include <stdio.h>
#include <iphlpapi.h>
#include <icmpapi.h>
#pragma comment(lib, "IPHLPAPI.lib")

void main()
{
    HANDLE hIcmpFile;

    hIcmpFile = Icmp6CreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE) {
      printf("\tUnable to open handle.\n");
      printf("Icmp6Createfile returned error: %ld\n", GetLastError() );
    }
    else
      printf("\tHandle created.\n");
}

```

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>
