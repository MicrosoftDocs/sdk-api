---
UID: NF:iphlpapi.GetIpStatistics
title: GetIpStatistics function (iphlpapi.h)
description: The GetIpStatistics function retrieves the IP statistics for the current computer.
helpviewer_keywords: ["GetIpStatistics","GetIpStatistics function [IP Helper]","_iphlp_getipstatistics","iphlp.getipstatistics","iphlpapi/GetIpStatistics"]
old-location: iphlp\getipstatistics.htm
tech.root: IpHlp
ms.assetid: 15daaa34-2011-462a-9543-f8d7ccb9f6fd
ms.date: 12/05/2018
ms.keywords: GetIpStatistics, GetIpStatistics function [IP Helper], _iphlp_getipstatistics, iphlp.getipstatistics, iphlpapi/GetIpStatistics
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
 - GetIpStatistics
 - iphlpapi/GetIpStatistics
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
 - GetIpStatistics
---

# GetIpStatistics function


## -description

The 
<b>GetIpStatistics</b> function retrieves the IP statistics for the current computer.

## -parameters

### -param Statistics [out]

A pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipstats_lh">MIB_IPSTATS</a> structure that receives the IP statistics for the local computer.

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
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatistics">GetIpStatistics</a> is unable to write to the memory pointed to by the <i>pStats</i> parameter.

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
<b>GetIpStatistics</b> function returns the statistics for IPv4 on the current computer.     On Windows XP and later, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a> can be used to obtain the IP statistics for either IPv4 or IPv6.


#### Examples

The following example retrieves the IPv4 statistics for the local computer and prints values from the returned data.


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

    DWORD dwRetval;
    MIB_IPSTATS *pStats;

    pStats = (MIB_IPSTATS *) MALLOC(sizeof (MIB_IPSTATS));

    if (pStats == NULL) {
        wprintf(L"Unable to allocate memory for MIB_IPSTATS\n");
        exit(1);
    }
    dwRetval = GetIpStatistics(pStats);
    if (dwRetval != NO_ERROR) {
        wprintf(L"GetIpStatistics call failed with %d\n", dwRetval);
        exit(1);
    } else {

        wprintf(L"IP forwarding: \t\t" );
        switch (pStats->dwForwarding) {
        case MIB_IP_FORWARDING: 
            wprintf(L"Enabled\n");
            break;
        case MIB_IP_NOT_FORWARDING: 
            wprintf(L"Disabled\n");
            break;
        default: 
            wprintf(L"unknown value = %d\n", pStats->dwForwarding);
            break;
        }
        
        wprintf(L"Default initial TTL: \t\t\t\t\t%u\n", pStats->dwDefaultTTL);

        wprintf(L"Number of received datagrams: \t\t\t\t%u\n", pStats->dwInReceives);
        wprintf(L"Number of received datagrams with header errors: \t%u\n", pStats->dwInHdrErrors);
        wprintf(L"Number of received datagrams with address errors: \t%u\n", pStats->dwInAddrErrors);

        wprintf(L"Number of datagrams forwarded: \t\t\t\t%ld\n", pStats->dwForwDatagrams);

        wprintf(L"Number of received datagrams with an unknown protocol: \t%u\n", pStats->dwInUnknownProtos);
        wprintf(L"Number of received datagrams discarded: \t\t%u\n", pStats->dwInDiscards);
        wprintf(L"Number of received datagrams delivered: \t\t%u\n", pStats->dwInDelivers);

        wprintf(L"Number of outgoing datagrams requested to transmit: \t%u\n", pStats->dwOutRequests);
        wprintf(L"Number of outgoing datagrams discarded for routing: \t%u\n", pStats->dwRoutingDiscards);
        wprintf(L"Number of outgoing datagrams discarded: \t\t%u\n", pStats->dwOutDiscards);
        wprintf(L"Number of outgoing datagrams with no route to destination discarded: %u\n", pStats->dwOutNoRoutes);

        wprintf(L"Fragment reassembly timeout: \t\t\t\t%u\n", pStats->dwReasmTimeout);
        wprintf(L"Number of datagrams that required reassembly: \t\t%u\n", pStats->dwReasmReqds);
        wprintf(L"Number of datagrams successfully reassembled: \t\t%u\n", pStats->dwReasmOks);
        wprintf(L"Number of datagrams that could not be reassembled: \t%u\n", pStats->dwReasmFails);

        wprintf(L"Number of datagrams fragmented successfully: \t\t%u\n", pStats->dwFragOks);
        wprintf(L"Number of datagrams not fragmented and discarded: \t%u\n", pStats->dwFragFails);
        wprintf(L"Number of fragments created: \t\t\t\t%u\n", pStats->dwFragCreates);

        wprintf(L"Number of interfaces: \t\t\t\t\t%u\n", pStats->dwNumIf);
        wprintf(L"Number of IP addresses: \t\t\t\t%u\n", pStats->dwNumAddr);
        wprintf(L"Number of routes: \t\t\t\t\t%u\n", pStats->dwNumRoutes);
    }

// Free memory allocated for the MIB_IPSTATS structure
    if (pStats)
        FREE(pStats);

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipstats_lh">MIB_IPSTATS</a>