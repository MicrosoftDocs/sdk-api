---
UID: NF:iphlpapi.GetTcpStatisticsEx
title: GetTcpStatisticsEx function (iphlpapi.h)
author: windows-sdk-content
description: The GetTcpStatisticsEx function retrieves the Transmission Control Protocol (TCP) statistics for the current computer.
old-location: iphlp\gettcpstatisticsex.htm
tech.root: IpHlp
ms.assetid: 78cfc69d-eae8-49c1-a460-6527a61f773d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetTcpStatisticsEx, GetTcpStatisticsEx function [IP Helper], _iphlp_gettcpstatisticsex, iphlp.gettcpstatisticsex, iphlpapi/GetTcpStatisticsEx
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetTcpStatisticsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTcpStatisticsEx function


## -description


The 
<b>GetTcpStatisticsEx</b> function retrieves the Transmission Control Protocol (TCP) statistics for the current computer. The 
<b>GetTcpStatisticsEx</b> function differs from the 
<b>GetTcpStatistics</b> function in that 
<b>GetTcpStatisticsEx</b> also supports the Internet Protocol version 6 (IPv6) protocol family.


## -parameters




### -param Statistics [out]

A pointer to a 
<a href="https://msdn.microsoft.com/08d85d02-62a0-479d-bf56-5dad452436f3">MIB_TCPSTATS</a> structure that receives the TCP statistics for the local computer.


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
The <i>pStats</i> parameter is <b>NULL</b> or does not point to valid memory, or the <i>dwFamily</i> parameter is not a valid value.

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



<a href="https://msdn.microsoft.com/841cdeaa-6284-4b39-a218-69937eca1982">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/9de7fa95-6bda-4fcc-b563-aed2e61fc1c7">GetUdpStatisticsEx</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/08d85d02-62a0-479d-bf56-5dad452436f3">MIB_TCPSTATS</a>
 

 

