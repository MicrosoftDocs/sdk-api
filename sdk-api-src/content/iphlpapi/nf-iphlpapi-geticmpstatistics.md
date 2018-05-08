---
UID: NF:iphlpapi.GetIcmpStatistics
title: GetIcmpStatistics function
author: windows-driver-content
description: The GetIcmpStatistics function retrieves the Internet Control Message Protocol (ICMP) for IPv4 statistics for the local computer.
old-location: iphlp\geticmpstatistics.htm
old-project: IpHlp
ms.assetid: b10ec58b-54fe-4068-beb9-6909ad7cecf7
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetIcmpStatistics, GetIcmpStatistics function [IP Helper], _iphlp_geticmpstatistics, iphlp.geticmpstatistics, iphlpapi/GetIcmpStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetIcmpStatistics
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIcmpStatistics function


## -description


The 
<b>GetIcmpStatistics</b> function retrieves the Internet Control Message Protocol (ICMP) for IPv4 statistics for the local computer.


## -parameters




### -param Statistics

TBD




#### - pStats [out]

A pointer to a 
<a href="https://msdn.microsoft.com/45ccaacb-f2cd-4be5-94ef-48d4403d5f60">MIB_ICMP</a> structure that receives the ICMP statistics for the local computer.


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
<a href="https://msdn.microsoft.com/b10ec58b-54fe-4068-beb9-6909ad7cecf7">GetIcmpStatistics</a> is unable to write to the memory pointed to by the <i>pStats</i> parameter.

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
<b>GetIcmpStatistics</b> function returns the ICMP statistics for IPv4 on the local computer.     On Windows XP and later, the <a href="https://msdn.microsoft.com/da9143cd-ccc9-4229-aa1e-d9949bbcb736">GetIpStatisticsEx</a> can be used to obtain the ICMP statistics for either IPv4 or IPv6 on the local computer.


#### Examples

The following example retrieves the ICMP for IPv4 statistics for the local computer and prints some information from the returned data.

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
                pIcmpStats-&gt;stats.icmpInStats.dwMsgs);
        wprintf(L"Number of incoming ICMP errors received: %ld\n",
                pIcmpStats-&gt;stats.icmpInStats.dwErrors);
        wprintf(L"Number of outgoing ICMP messages: %ld\n",
                pIcmpStats-&gt;stats.icmpOutStats.dwMsgs);
        wprintf(L"Number of outgoing ICMP errors sent: %ld\n",
                pIcmpStats-&gt;stats.icmpOutStats.dwErrors);
    } else {
        wprintf(L"GetIcmpStatistics failed with error: %ld\n", dwRetVal);
    }

    if (pIcmpStats)
        FREE(pIcmpStats);

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/15daaa34-2011-462a-9543-f8d7ccb9f6fd">GetIpStatistics</a>



<a href="https://msdn.microsoft.com/da9143cd-ccc9-4229-aa1e-d9949bbcb736">GetIpStatisticsEx</a>



<a href="https://msdn.microsoft.com/841cdeaa-6284-4b39-a218-69937eca1982">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/45ccaacb-f2cd-4be5-94ef-48d4403d5f60">MIB_ICMP</a>
 

 

