---
UID: NF:icmpapi.IcmpCreateFile
title: IcmpCreateFile function (icmpapi.h)
description: The IcmpCreateFile function opens a handle on which IPv4 ICMP echo requests can be issued.
helpviewer_keywords: ["IcmpCreateFile","IcmpCreateFile function [IP Helper]","_iphlp_icmpcreatefile","icmpapi/IcmpCreateFile","iphlp.icmpcreatefile"]
old-location: iphlp\icmpcreatefile.htm
tech.root: IpHlp
ms.assetid: b435b38b-df86-4991-9772-c712c9ea606f
ms.date: 12/05/2018
ms.keywords: IcmpCreateFile, IcmpCreateFile function [IP Helper], _iphlp_icmpcreatefile, icmpapi/IcmpCreateFile, iphlp.icmpcreatefile
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IcmpCreateFile
 - icmpapi/IcmpCreateFile
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
 - IcmpCreateFile
---

# IcmpCreateFile function


## -description

The 
<b>IcmpCreateFile</b> function opens a handle on which IPv4 ICMP echo requests can be issued.



## -returns

The 
<b>IcmpCreateFile</b> function returns an open handle on success. On failure, the function returns <b>INVALID_HANDLE_VALUE</b>. Call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for extended error information.

## -remarks

The <b>IcmpCreateFile</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpCreateFile</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpCreateFile</b> in the <i>Iphlpapi.dll</i> with calls to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpCreateFile</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

For IPv6, use the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>, <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>, and <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a> functions.

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example opens a handle on which ICMP echo requests can be issued. 


```cpp
#include <windows.h>
#include <stdio.h>
#include <iphlpapi.h>
#include <icmpapi.h>

// Need to link with Iplhlapi.lib
#pragma comment(lib, "IPHLPAPI.lib")

void main()
{
    HANDLE hIcmpFile;

    hIcmpFile = IcmpCreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE) {
      printf("\tUnable to open handle.\n");
      printf("IcmpCreatefile returned error: %ld\n", GetLastError() );
    }
    else {
      printf("\tHandle created.\n");
      // Need to close the handle when done using it
      IcmpCloseHandle(hIcmpFile);
    }  
}

```

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpclosehandle">IcmpCloseHandle</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>
