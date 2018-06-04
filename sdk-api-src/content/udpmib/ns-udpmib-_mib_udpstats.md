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

# _MIB_UDPSTATS structure


## -description


The 
<b>MIB_UDPSTATS</b> structure contains statistics for the User Datagram Protocol (UDP) running on the local computer.


## -struct-fields




### -field dwInDatagrams

The number of datagrams received.


### -field dwNoPorts

The number of datagrams received that were discarded because the port specified was invalid.


### -field dwInErrors

The number of erroneous datagrams  received. This number does not include the value contained by the <b>dwNoPorts</b> member.


### -field dwOutDatagrams

The number of datagrams transmitted.


### -field dwNumAddrs

The number of entries in the UDP listener table.


## -remarks



The 
			<a href="_iphlp_getudpstatistics">GetUdpStatistics</a> function returns a pointer to a <b>MIB_UDPSTATS</b> structure. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="_iphlp_gettcpstatistics">GetTcpStatistics</a>



<a href="_iphlp_getudpstatistics">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a>
 

 

