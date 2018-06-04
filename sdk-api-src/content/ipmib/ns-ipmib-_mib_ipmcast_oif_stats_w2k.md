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

# _MIB_IPMCAST_OIF_STATS_W2K structure


## -description


The 
<b>MIB_IPMCAST_OIF_STATS</b> structure stores the statistics that are associated with an outgoing multicast interface.


## -struct-fields




### -field dwOutIfIndex

Type: <b>DWORD</b>

Specifies the outgoing interface to which these statistics are related.


### -field dwNextHopAddr

Type: <b>DWORD</b>

Specifies the address of the next hop that corresponds to <b>dwOutIfIndex</b>. The <b>dwOutIfIndex</b> and <b>dwIfNextHopIPAddr</b> members uniquely identify a next hop on point-to-multipoint interfaces, where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple-access (NBMA) interfaces, and the internal interface on which all dial-up clients connect. 




For Ethernet and other broadcast interfaces, specify zero. Also specify zero for point-to-point interfaces, which are identified by only <b>dwOutIfIndex</b>.


#### - pvDialContext

Type: <b>PVOID</b>

Reserved. This member should be <b>NULL</b>.


### -field ulTtlTooLow

Type: <b>ULONG</b>

Specifies the number of packets on this outgoing interface that were discarded because the packet's time-to-live (TTL) value was too low.


### -field ulFragNeeded

Type: <b>ULONG</b>

Specifies the number of packets that required fragmentation when they were forwarded on this interface.


### -field ulOutPackets

Type: <b>ULONG</b>

Specifies the number of packets that were forwarded out this interface.


### -field ulOutDiscards

Type: <b>ULONG</b>

Specifies the number of packets that were discarded on this interface.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40">MIB_IPMCAST_OIF</a>
 

 

