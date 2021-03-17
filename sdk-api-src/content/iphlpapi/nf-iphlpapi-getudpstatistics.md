---
UID: NF:iphlpapi.GetUdpStatistics
title: GetUdpStatistics function (iphlpapi.h)
description: The GetUdpStatistics function retrieves the User Datagram Protocol (UDP) statistics for the local computer.
helpviewer_keywords: ["GetUdpStatistics","GetUdpStatistics function [IP Helper]","_iphlp_getudpstatistics","iphlp.getudpstatistics","iphlpapi/GetUdpStatistics"]
old-location: iphlp\getudpstatistics.htm
tech.root: IpHlp
ms.assetid: a86e5758-a984-4483-8e9c-c482a7676a20
ms.date: 12/05/2018
ms.keywords: GetUdpStatistics, GetUdpStatistics function [IP Helper], _iphlp_getudpstatistics, iphlp.getudpstatistics, iphlpapi/GetUdpStatistics
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
 - GetUdpStatistics
 - iphlpapi/GetUdpStatistics
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
 - GetUdpStatistics
---

# GetUdpStatistics function


## -description

The 
<b>GetUdpStatistics</b> function retrieves the User Datagram Protocol (UDP) statistics for the local computer.

## -parameters

### -param Stats [out]

Pointer to a 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a> structure that receives the UDP statistics for the local computer.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -remarks

<b>Windows Server 2003 and Windows XP:  </b>Use the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a> function to obtain the UDP statistics for the IPv6 protocol.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipstatistics">GetIpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a>