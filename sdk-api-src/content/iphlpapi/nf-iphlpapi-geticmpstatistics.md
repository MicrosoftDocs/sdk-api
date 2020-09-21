---
UID: NF:iphlpapi.GetIcmpStatistics
title: GetIcmpStatistics function (iphlpapi.h)
description: The GetIcmpStatistics function retrieves the Internet Control Message Protocol (ICMP) for IPv4 statistics for the local computer.
helpviewer_keywords: ["GetIcmpStatistics","GetIcmpStatistics function [IP Helper]","_iphlp_geticmpstatistics","iphlp.geticmpstatistics","iphlpapi/GetIcmpStatistics"]
old-location: iphlp\geticmpstatistics.htm
tech.root: IpHlp
ms.assetid: b10ec58b-54fe-4068-beb9-6909ad7cecf7
ms.date: 12/05/2018
ms.keywords: GetIcmpStatistics, GetIcmpStatistics function [IP Helper], _iphlp_geticmpstatistics, iphlp.geticmpstatistics, iphlpapi/GetIcmpStatistics
req.header: iphlpapi.h
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
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIcmpStatistics
 - iphlpapi/GetIcmpStatistics
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
 - GetIcmpStatistics
---

# GetIcmpStatistics function


## -description

The 
<b>GetIcmpStatistics</b> function retrieves the Internet Control Message Protocol (ICMP) for IPv4 statistics for the local computer.

## -parameters

### -param Statistics [out]

A pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp">MIB_ICMP</a> structure that receives the ICMP statistics for the local computer.

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
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a> is unable to write to the memory pointed to by the <i>pStats</i> parameter.

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
<b>GetIcmpStatistics</b> function returns the ICMP statistics for IPv4 on the local computer.     On Windows XP and later, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a> can be used to obtain the ICMP statistics for either IPv4 or IPv6 on the local computer.


#### Examples

The following example retrieves the ICMP for IPv4 statistics for the local computer and prints some information from the returned data.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

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

    DWORD dwRetVal = 0;
    PMIB_ICMP pIcmpStats;

    pIcmpStats = (MIB_ICMP *) MALLOC(sizeof (MIB_ICMP));
    if (pIcmpStats == NULL) {
        wprintf(L"Error allocating memory\n");
        return 1;
    }

    dwRetVal = GetIcmpStatistics(pIcmpStats);
    if (dwRetVal == NO_ERROR) {
        wprintf(L"Number of incoming ICMP messages: %ld\n",
                pIcmpStats->stats.icmpInStats.dwMsgs);
        wprintf(L"Number of incoming ICMP errors received: %ld\n",
                pIcmpStats->stats.icmpInStats.dwErrors);
        wprintf(L"Number of outgoing ICMP messages: %ld\n",
                pIcmpStats->stats.icmpOutStats.dwMsgs);
        wprintf(L"Number of outgoing ICMP errors sent: %ld\n",
                pIcmpStats->stats.icmpOutStats.dwErrors);
    } else {
        wprintf(L"GetIcmpStatistics failed with error: %ld\n", dwRetVal);
    }

    if (pIcmpStats)
        FREE(pIcmpStats);

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatistics">GetIpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp">MIB_ICMP</a>