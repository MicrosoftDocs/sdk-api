---
UID: NF:iphlpapi.GetUdpStatisticsEx2
title: GetUdpStatisticsEx2 function (iphlpapi.h)
author: windows-sdk-content
description: The GetUdpStatisticsEx2 function retrieves the User Datagram Protocol (UDP) statistics for the current computer.
old-location: iphlp\getudpstatisticsex2.htm
tech.root: IpHlp
ms.assetid: 8DE392C5-90EF-490D-B53A-58D75A854138
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetUdpStatisticsEx2, GetUdpStatisticsEx2 function [IP Helper], iphlp.getudpstatisticsex2, iphlpapi/GetUdpStatisticsEx2
ms.topic: function
f1_keywords:
- iphlpapi/GetUdpStatisticsEx2
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iphlpapi.dll
api_name:
- GetUdpStatisticsEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUdpStatisticsEx2 function


## -description


The 
<b>GetUdpStatisticsEx2</b> function retrieves the User Datagram Protocol (UDP) statistics for the current computer. The 
<b>GetUdpStatisticsEx2</b> function differs from the 
<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a> function in that 
<b>GetUdpStatisticsEx2</b> uses a new output structure that contains 64-bit counters, rather than 32-bit counters.


## -parameters




### -param Statistics [out]

A pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Mt804346(v=VS.85).aspx">MIB_UDPSTATS2</a> structure that receives the UDP statistics for the local computer.


### -param Family [in]

The protocol family for which to retrieve statistics. This parameter must be one of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
Internet Protocol version 4 (IPv4).

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
Internet Protocol version 6 (IPv6).

</td>
</tr>
</table>
 


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
The <i>Statistics</i> parameter is <b>NULL</b> or does not point to valid memory, or the <i>Family</i> parameter is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system on which the function call was made.

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
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a>
 

 

