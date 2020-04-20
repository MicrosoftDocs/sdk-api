---
UID: NF:iphlpapi.GetTcpStatisticsEx2
title: GetTcpStatisticsEx2 function (iphlpapi.h)
description: The GetTcpStatisticsEx2 function retrieves the Transmission Control Protocol (TCP) statistics for the current computer.helpviewer_keywords: ["AF_INET","AF_INET6","GetTcpStatisticsEx2","GetTcpStatisticsEx2 function [IP Helper]","iphlp.gettcpstatisticsex2","iphlpapi/GetTcpStatisticsEx2"]
old-location: iphlp\gettcpstatisticsex2.htm
tech.root: IpHlp
ms.assetid: E7D988E3-4CE9-4BD3-96C7-4C16D2D6FA9C
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetTcpStatisticsEx2, GetTcpStatisticsEx2 function [IP Helper], iphlp.gettcpstatisticsex2, iphlpapi/GetTcpStatisticsEx2
f1_keywords:
- iphlpapi/GetTcpStatisticsEx2
dev_langs:
- c++
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
- GetTcpStatisticsEx2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTcpStatisticsEx2 function


## -description


The 
<b>GetTcpStatisticsEx2</b> function retrieves the Transmission Control Protocol (TCP) statistics for the current computer. The 
<b>GetTcpStatisticsEx2</b> function differs from the 
<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a> function in that 
it uses a new output structure that contains 64-bit counters, rather than 32-bit counters.


## -parameters




### -param Statistics [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcpstats_lh">MIB_TCPSTATS2</a> structure that receives the TCP statistics for the local computer.


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
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>
 

 

