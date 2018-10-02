---
UID: NF:iphlpapi.GetUdpStatisticsEx2
title: GetUdpStatisticsEx2 function
author: windows-sdk-content
description: The GetUdpStatisticsEx2 function retrieves the User Datagram Protocol (UDP) statistics for the current computer.
old-location: iphlp\getudpstatisticsex2.htm
tech.root: IpHlp
ms.assetid: 8DE392C5-90EF-490D-B53A-58D75A854138
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AF_INET, AF_INET6, GetUdpStatisticsEx2, GetUdpStatisticsEx2 function [IP Helper], iphlp.getudpstatisticsex2, iphlpapi/GetUdpStatisticsEx2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
---

# GetUdpStatisticsEx2 function


## -description


The 
<b>GetUdpStatisticsEx2</b> function retrieves the User Datagram Protocol (UDP) statistics for the current computer. The 
<b>GetUdpStatisticsEx2</b> function differs from the 
<a href="https://msdn.microsoft.com/9de7fa95-6bda-4fcc-b563-aed2e61fc1c7">GetUdpStatisticsEx</a> function in that 
<b>GetUdpStatisticsEx2</b> uses a new output structure that contains 64-bit counters, rather than 32-bit counters.


## -parameters




### -param Statistics [out]

A pointer to a 
<a href="https://msdn.microsoft.com/A225E0E7-54FB-4655-9A45-F3EF6DA1FF4E">MIB_UDPSTATS2</a> structure that receives the UDP statistics for the local computer.


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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da9143cd-ccc9-4229-aa1e-d9949bbcb736">GetIpStatisticsEx</a>



<a href="https://msdn.microsoft.com/78cfc69d-eae8-49c1-a460-6527a61f773d">GetTcpStatisticsEx</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a>
 

 

