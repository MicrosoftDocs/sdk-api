---
UID: NF:iphlpapi.GetIcmpStatisticsEx
title: GetIcmpStatisticsEx function (iphlpapi.h)
description: The GetIcmpStatisticsEx function retrieves Internet Control Message Protocol (ICMP) statistics for the local computer. The GetIcmpStatisticsEx function is capable of retrieving IPv6 ICMP statistics.
helpviewer_keywords: ["AF_INET","AF_INET6","GetIcmpStatisticsEx","GetIcmpStatisticsEx function [IP Helper]","iphlp.geticmpstatisticsex","iphlpapi/GetIcmpStatisticsEx"]
old-location: iphlp\geticmpstatisticsex.htm
tech.root: IpHlp
ms.assetid: b074650a-0f03-448c-8828-c7bcec9d6030
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetIcmpStatisticsEx, GetIcmpStatisticsEx function [IP Helper], iphlp.geticmpstatisticsex, iphlpapi/GetIcmpStatisticsEx
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
 - GetIcmpStatisticsEx
 - iphlpapi/GetIcmpStatisticsEx
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
 - GetIcmpStatisticsEx
---

# GetIcmpStatisticsEx function


## -description

The <b>GetIcmpStatisticsEx</b> function retrieves  Internet Control Message Protocol (ICMP) statistics for the local computer. The <b>GetIcmpStatisticsEx</b> function is capable of retrieving IPv6 ICMP statistics.

## -parameters

### -param Statistics [out]

A pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a> structure that contains ICMP statistics for the local computer.

### -param Family [in]

The protocol family for which to retrieve ICMP statistics. Must be one of the following: 



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

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatisticsex">GetIpStatisticsEx</a> can be used to obtain the ICMP statistics for either IPv4 or IPv6 on the local computer. 

The 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a> function returns the ICMP statistics for only IPv4 on the local computer.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a>