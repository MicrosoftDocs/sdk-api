---
UID: NF:lmremutl.NetRemoteTOD
title: NetRemoteTOD function (lmremutl.h)
description: The NetRemoteTOD function returns the time of day information from a specified server.
helpviewer_keywords: ["NetRemoteTOD","NetRemoteTOD function [Network Management]","_win32_netremotetod","lmremutl/NetRemoteTOD","netmgmt.netremotetod"]
old-location: netmgmt\netremotetod.htm
tech.root: NetMgmt
ms.assetid: 5a935e09-f188-4ee1-b998-c67488475baa
ms.date: 12/05/2018
ms.keywords: NetRemoteTOD, NetRemoteTOD function [Network Management], _win32_netremotetod, lmremutl/NetRemoteTOD, netmgmt.netremotetod
req.header: lmremutl.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetRemoteTOD
 - lmremutl/NetRemoteTOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetRemoteTOD
---

# NetRemoteTOD function


## -description

The
				<b>NetRemoteTOD</b> function returns the time of day information from a specified server.

## -parameters

### -param UncServerName [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param BufferPtr [out]

Pointer to the address that receives the 
<a href="/windows/desktop/api/lmremutl/ns-lmremutl-time_of_day_info">TIME_OF_DAY_INFO</a> information structure. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to successfully execute the 
<b>NetRemoteTOD</b> function.


#### Examples

The following code sample demonstrates how to retrieve and print the current date and time with a call to the 
<b>NetRemoteTOD</b> function. To do this, the sample uses the 
<a href="/windows/desktop/api/lmremutl/ns-lmremutl-time_of_day_info">TIME_OF_DAY_INFO</a> structure. Finally, the sample frees the memory allocated for the information buffer.


```cpp
#include <stdio.h>
#include <windows.h> 
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

#ifndef UNICODE
#define UNICODE
#endif

int wmain(int argc, wchar_t *argv[])
{
   LPTIME_OF_DAY_INFO pBuf = NULL;
   NET_API_STATUS nStatus;
   LPTSTR pszServerName = NULL;

   if (argc > 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = (LPTSTR) argv[1];
   //
   // Call the NetRemoteTOD function.
   //
   nStatus = NetRemoteTOD((LPCWSTR) pszServerName,
                          (LPBYTE *)&pBuf);
   //
   // If the function succeeds, display the current date and time.
   //
   if (nStatus == NERR_Success)
   {
      if (pBuf != NULL)
      {
         fprintf(stderr, "\nThe current date is: %d/%d/%d\n",
                 pBuf->tod_month, pBuf->tod_day, pBuf->tod_year);
         fprintf(stderr, "The current time is: %d:%d:%d\n",
                 pBuf->tod_hours, pBuf->tod_mins, pBuf->tod_secs);
      }
   }
   //
   // Otherwise, display a system error.
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);
   //
   // Free the allocated buffer.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/remote-utility-functions">Remote
		  Utility Functions</a>



<a href="/windows/desktop/api/lmremutl/ns-lmremutl-time_of_day_info">TIME_OF_DAY_INFO</a>