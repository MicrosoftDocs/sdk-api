---
UID: NF:iphlpapi.GetUdpStatisticsEx
title: GetUdpStatisticsEx function (iphlpapi.h)
description: The GetUdpStatisticsEx function retrieves the User Datagram Protocol (UDP) statistics for the current computer.
helpviewer_keywords: ["AF_INET","AF_INET6","GetUdpStatisticsEx","GetUdpStatisticsEx function [IP Helper]","_iphlp_getudpstatisticsex","iphlp.getudpstatisticsex","iphlpapi/GetUdpStatisticsEx"]
old-location: iphlp\getudpstatisticsex.htm
tech.root: IpHlp
ms.assetid: 9de7fa95-6bda-4fcc-b563-aed2e61fc1c7
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetUdpStatisticsEx, GetUdpStatisticsEx function [IP Helper], _iphlp_getudpstatisticsex, iphlp.getudpstatisticsex, iphlpapi/GetUdpStatisticsEx
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetUdpStatisticsEx
 - iphlpapi/GetUdpStatisticsEx
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
 - GetUdpStatisticsEx
---

# GetUdpStatisticsEx function


## -description

The 
<b>GetUdpStatisticsEx</b> function retrieves the User Datagram Protocol (UDP) statistics for the current computer. The 
<b>GetUdpStatisticsEx</b> function differs from the 
<b>GetUdpStatistics</b> function in that 
<b>GetUdpStatisticsEx</b> also supports the Internet Protocol version 6 (IPv6) protocol family.

## -parameters

### -param Statistics [out]

A pointer to a 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a> structure that receives the UDP statistics for the local computer.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a>