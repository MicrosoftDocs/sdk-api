---
UID: NF:iphlpapi.GetIpStatistics
title: GetIpStatistics function
author: windows-sdk-content
description: The GetIpStatistics function retrieves the IP statistics for the current computer.
old-location: iphlp\getipstatistics.htm
old-project: IpHlp
ms.assetid: 15daaa34-2011-462a-9543-f8d7ccb9f6fd
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetIpStatistics, GetIpStatistics function [IP Helper], _iphlp_getipstatistics, iphlp.getipstatistics, iphlpapi/GetIpStatistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpStatistics
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIpStatistics function


## -description


The 
<b>GetIpStatistics</b> function retrieves the IP statistics for the current computer.


## -parameters




### -param Statistics

TBD




#### - pStats [out]

A pointer to a 
<a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a> structure that receives the IP statistics for the local computer.


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
<a href="https://msdn.microsoft.com/15daaa34-2011-462a-9543-f8d7ccb9f6fd">GetIpStatistics</a> is unable to write to the memory pointed to by the <i>pStats</i> parameter.

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
the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The 
<b>GetIpStatistics</b> function returns the statistics for IPv4 on the current computer.     On Windows XP and later, the <a href="https://msdn.microsoft.com/da9143cd-ccc9-4229-aa1e-d9949bbcb736">GetIpStatisticsEx</a> can be used to obtain the IP statistics for either IPv4 or IPv6.


#### Examples

The following example retrieves the IPv4 statistics for the local computer and prints values from the returned data.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;

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
        switch (pStats-&gt;dwForwarding) {
        case MIB_IP_FORWARDING: 
            wprintf(L"Enabled\n");
            break;
        case MIB_IP_NOT_FORWARDING: 
            wprintf(L"Disabled\n");
            break;
        default: 
            wprintf(L"unknown value = %d\n", pStats-&gt;dwForwarding);
            break;
        }
        
        wprintf(L"Default initial TTL: \t\t\t\t\t%u\n", pStats-&gt;dwDefaultTTL);

        wprintf(L"Number of received datagrams: \t\t\t\t%u\n", pStats-&gt;dwInReceives);
        wprintf(L"Number of received datagrams with header errors: \t%u\n", pStats-&gt;dwInHdrErrors);
        wprintf(L"Number of received datagrams with address errors: \t%u\n", pStats-&gt;dwInAddrErrors);

        wprintf(L"Number of datagrams forwarded: \t\t\t\t%ld\n", pStats-&gt;dwForwDatagrams);

        wprintf(L"Number of received datagrams with an unknown protocol: \t%u\n", pStats-&gt;dwInUnknownProtos);
        wprintf(L"Number of received datagrams discarded: \t\t%u\n", pStats-&gt;dwInDiscards);
        wprintf(L"Number of received datagrams delivered: \t\t%u\n", pStats-&gt;dwInDelivers);

        wprintf(L"Number of outgoing datagrams requested to transmit: \t%u\n", pStats-&gt;dwOutRequests);
        wprintf(L"Number of outgoing datagrams discarded for routing: \t%u\n", pStats-&gt;dwRoutingDiscards);
        wprintf(L"Number of outgoing datagrams discarded: \t\t%u\n", pStats-&gt;dwOutDiscards);
        wprintf(L"Number of outgoing datagrams with no route to destination discarded: %u\n", pStats-&gt;dwOutNoRoutes);

        wprintf(L"Fragment reassembly timeout: \t\t\t\t%u\n", pStats-&gt;dwReasmTimeout);
        wprintf(L"Number of datagrams that required reassembly: \t\t%u\n", pStats-&gt;dwReasmReqds);
        wprintf(L"Number of datagrams successfully reassembled: \t\t%u\n", pStats-&gt;dwReasmOks);
        wprintf(L"Number of datagrams that could not be reassembled: \t%u\n", pStats-&gt;dwReasmFails);

        wprintf(L"Number of datagrams fragmented successfully: \t\t%u\n", pStats-&gt;dwFragOks);
        wprintf(L"Number of datagrams not fragmented and discarded: \t%u\n", pStats-&gt;dwFragFails);
        wprintf(L"Number of fragments created: \t\t\t\t%u\n", pStats-&gt;dwFragCreates);

        wprintf(L"Number of interfaces: \t\t\t\t\t%u\n", pStats-&gt;dwNumIf);
        wprintf(L"Number of IP addresses: \t\t\t\t%u\n", pStats-&gt;dwNumAddr);
        wprintf(L"Number of routes: \t\t\t\t\t%u\n", pStats-&gt;dwNumRoutes);
    }

// Free memory allocated for the MIB_IPSTATS structure
    if (pStats)
        FREE(pStats);

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b10ec58b-54fe-4068-beb9-6909ad7cecf7">GetIcmpStatistics</a>



<a href="https://msdn.microsoft.com/da9143cd-ccc9-4229-aa1e-d9949bbcb736">GetIpStatisticsEx</a>



<a href="https://msdn.microsoft.com/841cdeaa-6284-4b39-a218-69937eca1982">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a>
 

 

