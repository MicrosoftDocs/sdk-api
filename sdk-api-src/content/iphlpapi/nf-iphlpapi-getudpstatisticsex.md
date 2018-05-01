---
UID: NF:iphlpapi.GetUdpStatisticsEx
title: GetUdpStatisticsEx function
author: windows-driver-content
description: The GetUdpStatisticsEx function retrieves the User Datagram Protocol (UDP) statistics for the current computer.
old-location: iphlp\getudpstatisticsex.htm
old-project: IpHlp
ms.assetid: 9de7fa95-6bda-4fcc-b563-aed2e61fc1c7
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AF_INET, AF_INET6, GetUdpStatisticsEx, GetUdpStatisticsEx function [IP Helper], _iphlp_getudpstatisticsex, iphlp.getudpstatisticsex, iphlpapi/GetUdpStatisticsEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
-	GetUdpStatisticsEx
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetUdpStatisticsEx function


## -description



			The 
<b>GetUdpStatisticsEx</b> function retrieves the User Datagram Protocol (UDP) statistics for the current computer. The 
<b>GetUdpStatisticsEx</b> function differs from the 
<b>GetUdpStatistics</b> function in that 
<b>GetUdpStatisticsEx</b> also supports the Internet Protocol version 6 (IPv6) protocol family.
		


## -parameters




### -param Statistics

TBD


### -param Family

TBD




#### - dwFamily [in]

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
 


#### - pStats [out]

A pointer to a 
<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a> structure that receives the UDP statistics for the local computer.


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



<a href="https://msdn.microsoft.com/78cfc69d-eae8-49c1-a460-6527a61f773d">GetTcpStatisticsEx</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a>
 

 

