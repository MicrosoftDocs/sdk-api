---
UID: NF:iphlpapi.GetUdpStatistics
title: GetUdpStatistics function
author: windows-sdk-content
description: The GetUdpStatistics function retrieves the User Datagram Protocol (UDP) statistics for the local computer.
old-location: iphlp\getudpstatistics.htm
old-project: IpHlp
ms.assetid: a86e5758-a984-4483-8e9c-c482a7676a20
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetUdpStatistics, GetUdpStatistics function [IP Helper], _iphlp_getudpstatistics, iphlp.getudpstatistics, iphlpapi/GetUdpStatistics
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetUdpStatistics
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetUdpStatistics function


## -description


The 
<b>GetUdpStatistics</b> function retrieves the User Datagram Protocol (UDP) statistics for the local computer.


## -parameters




### -param Stats

TBD




#### - pStats [out]

Pointer to a 
<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a> structure that receives the UDP statistics for the local computer.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -remarks



<b>Windows Server 2003 and Windows XP:  </b>Use the 
<a href="https://msdn.microsoft.com/9de7fa95-6bda-4fcc-b563-aed2e61fc1c7">GetUdpStatisticsEx</a> function to obtain the UDP statistics for the IPv6 protocol.




## -see-also




<a href="https://msdn.microsoft.com/b10ec58b-54fe-4068-beb9-6909ad7cecf7">GetIcmpStatistics</a>



<a href="https://msdn.microsoft.com/15daaa34-2011-462a-9543-f8d7ccb9f6fd">GetIpStatistics</a>



<a href="https://msdn.microsoft.com/841cdeaa-6284-4b39-a218-69937eca1982">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/9de7fa95-6bda-4fcc-b563-aed2e61fc1c7">GetUdpStatisticsEx</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a>
 

 

