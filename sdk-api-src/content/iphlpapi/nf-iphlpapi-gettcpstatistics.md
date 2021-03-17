---
UID: NF:iphlpapi.GetTcpStatistics
title: GetTcpStatistics function (iphlpapi.h)
description: The GetTcpStatistics function retrieves the TCP statistics for the local computer.
helpviewer_keywords: ["GetTcpStatistics","GetTcpStatistics function [IP Helper]","_iphlp_gettcpstatistics","iphlp.gettcpstatistics","iphlpapi/GetTcpStatistics"]
old-location: iphlp\gettcpstatistics.htm
tech.root: IpHlp
ms.assetid: 841cdeaa-6284-4b39-a218-69937eca1982
ms.date: 12/05/2018
ms.keywords: GetTcpStatistics, GetTcpStatistics function [IP Helper], _iphlp_gettcpstatistics, iphlp.gettcpstatistics, iphlpapi/GetTcpStatistics
req.header: iphlpapi.h
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
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTcpStatistics
 - iphlpapi/GetTcpStatistics
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
 - GetTcpStatistics
---

# GetTcpStatistics function


## -description

The 
<b>GetTcpStatistics</b> function retrieves the TCP statistics for the local computer.

## -parameters

### -param Statistics [out]

A pointer to a 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcpstats_lh">MIB_TCPSTATS</a> structure that receives the TCP statistics for the local computer.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStats</i> parameter is <b>NULL</b>, or 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a> is unable to write to the memory pointed to by the <i>pStats</i> parameter.

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
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The 
<b>GetTcpStatistics</b> function returns the TCP statistics for IPv4 on the current computer.     On Windows XP and later, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a> can be used to obtain the TCP statistics for either IPv4 or IPv6.


#### Examples

The following example retrieves the TCP statistics for the local computer and prints some values from the returned data.


```cpp
//#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x)) 
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int main()
{
    PMIB_TCPSTATS pTCPStats;
    DWORD dwRetVal = 0;

    pTCPStats = (MIB_TCPSTATS*) MALLOC (sizeof(MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
        return 1;
    }

    if ((dwRetVal = GetTcpStatistics(pTCPStats)) == NO_ERROR) {
      printf("\tActive Opens: %ld\n", pTCPStats->dwActiveOpens);
      printf("\tPassive Opens: %ld\n", pTCPStats->dwPassiveOpens);
      printf("\tSegments Recv: %ld\n", pTCPStats->dwInSegs);
      printf("\tSegments Xmit: %ld\n", pTCPStats->dwOutSegs);
      printf("\tTotal # Conxs: %ld\n", pTCPStats->dwNumConns);
    }
    else {
      printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
      
      LPVOID lpMsgBuf;
      if (FormatMessage( FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM | 
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dwRetVal,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
        (LPTSTR) &lpMsgBuf,
        0,
        NULL )) {
        printf("\tError: %s", lpMsgBuf);
      }
      LocalFree( lpMsgBuf );
    }

    if (pTCPStats)
        FREE (pTCPStats);
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatistics">GetIpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcpstats_lh">MIB_TCPSTATS</a>