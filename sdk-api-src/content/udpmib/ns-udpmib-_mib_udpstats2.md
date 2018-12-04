---
UID: NS:udpmib._MIB_UDPSTATS2
title: "_MIB_UDPSTATS2"
author: windows-sdk-content
description: Contains statistics for the User Datagram Protocol (UDP) running on the local computer.
old-location: mib\mib_udpstats2.htm
tech.root: MIB
ms.assetid: A225E0E7-54FB-4655-9A45-F3EF6DA1FF4E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMIB_UDPSTATS2, MIB_UDPSTATS2, MIB_UDPSTATS2 structure [MIB], PMIB_UDPSTATS2, PMIB_UDPSTATS2 structure pointer [MIB], _MIB_UDPSTATS2, mib.mib_udpstats2, udpmib/MIB_UDPSTATS, udpmib/PMIB_UDPSTATS2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: udpmib.h
req.include-header: Iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - udpmib.h
api_name:
 - MIB_UDPSTATS2
product: Windows
targetos: Windows
req.typenames: MIB_UDPSTATS2, *PMIB_UDPSTATS2
req.redist: 
---

# _MIB_UDPSTATS2 structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The 
<b>MIB_UDPSTATS2</b> structure contains statistics for the User Datagram Protocol (UDP) running on the local computer. This structure is different from <a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a> structure in that it uses 64-bit counters, rather than 32-bit counters.


## -struct-fields




### -field dw64InDatagrams

The number of datagrams received.


### -field dwNoPorts

The number of datagrams received that were discarded because the port specified was invalid.


### -field dwInErrors

The number of erroneous datagrams  received. This number does not include the value contained by the <b>dwNoPorts</b> member.


### -field dw64OutDatagrams

The number of datagrams transmitted.


### -field dwNumAddrs

The number of entries in the UDP listener table.


## -remarks



The 
			<a href="_iphlp_getudpstatisticsEx2">GetUdpStatisticsEx2</a> function returns a pointer to a <b>MIB_UDPSTATS2</b> structure. 




## -see-also




<a href="_iphlp_gettcpstatisticsEx2">GetTcpStatisticsEx2</a>



<a href="_iphlp_getudpstatisticsex2">GetUdpStatisticsEx2</a>



<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a>
 

 

