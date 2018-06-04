---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

