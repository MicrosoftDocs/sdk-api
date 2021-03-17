---
UID: NF:icmpapi.IcmpCloseHandle
title: IcmpCloseHandle function (icmpapi.h)
description: The IcmpCloseHandle function closes a handle opened by a call to the IcmpCreateFile or Icmp6CreateFile functions.
helpviewer_keywords: ["IcmpCloseHandle","IcmpCloseHandle function [IP Helper]","_iphlp_icmpclosehandle","icmpapi/IcmpCloseHandle","iphlp.icmpclosehandle"]
old-location: iphlp\icmpclosehandle.htm
tech.root: IpHlp
ms.assetid: ce8f11bb-1e33-41bd-adb9-c18efadd4d0b
ms.date: 12/05/2018
ms.keywords: IcmpCloseHandle, IcmpCloseHandle function [IP Helper], _iphlp_icmpclosehandle, icmpapi/IcmpCloseHandle, iphlp.icmpclosehandle
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
 - IcmpCloseHandle
 - icmpapi/IcmpCloseHandle
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
 - IcmpCloseHandle
---

# IcmpCloseHandle function


## -description

The 
<b>IcmpCloseHandle</b> function closes a handle opened by a call to 
the <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a> or <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a> functions.

## -parameters

### -param IcmpHandle [in]

The handle to close. This handle must have been returned by a call to <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a> or <a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>.

## -returns

If the handle is closed successfully the return value is <b>TRUE</b>, otherwise <b>FALSE</b>. Call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for extended error information.

## -remarks

The <b>IcmpCloseHandle</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpCloseHandle</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpCloseHandle</b> in the <i>Iphlpapi.dll</i> with calls to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpCloseHandle</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example opens and closes a handle on which ICMP echo requests can be issued. 


```cpp
#include <windows.h>
#include <iphlpapi.h>
#include <icmpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")

void main()
{
    HANDLE hIcmpFile;
    BOOL bRetVal; 

    hIcmpFile = IcmpCreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE)
      printf("IcmpCreateFile failed with error: %ld\n", GetLastError() );
    else 
    {
      printf("\tHandle created.\n");

      bRetVal = IcmpCloseHandle(hIcmpFile);
      if (bRetVal)
          printf("\tHandle was closed\n");
      else
          printf("IcmpCloseHandle failed with error: %ld\n", GetLastError() );
    }
}


```

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6createfile">Icmp6CreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6parsereplies">Icmp6ParseReplies</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmp6sendecho2">Icmp6SendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpcreatefile">IcmpCreateFile</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpparsereplies">IcmpParseReplies</a>



<b>IcmpSendEcho</b>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2ex">IcmpSendEcho2Ex</a>