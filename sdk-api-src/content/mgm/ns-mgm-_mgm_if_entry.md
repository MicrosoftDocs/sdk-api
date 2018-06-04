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

# _MGM_IF_ENTRY structure


## -description


The 
<b>MGM_IF_ENTRY</b> structure describes a router interface. This structure is used in the 
<a href="https://msdn.microsoft.com/1d161a7e-3ceb-429f-a41e-eccd7f98f084">PMGM_CREATION_ALERT_CALLBACK</a>. In the context of this callback, the routing protocol must enable or disable multicast forwarding on each interface, notifying the multicast group manager by using the <b>bIsEnabled</b> member.


## -struct-fields




### -field dwIfIndex

Specifies the index of the interface.


### -field dwIfNextHopAddr

Specifies the address of the next hop that corresponds to the index specified by <b>dwIfIndex</b>. The <b>dwIfIndex</b> and <b>dwIfNextHopIPAddr</b> members uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <b>dwIfIndex</b>, specify zero.


### -field bIGMP

Indicates whether or not IGMP is enabled on this interface. If <b>bIGMP</b> is <b>TRUE</b>, then IGMP is enabled on this interface. If <b>bIGMP</b> is <b>FALSE</b>, then IGMP is not enabled on this interface.


### -field bIsEnabled

Indicates whether or not multicast forwarding is enabled on this interface. If <b>bIsEnabled</b> is <b>TRUE</b>, multicast forwarding is enabled on this interface. If <b>bIsEnabled</b> is <b>FALSE</b>, multicast forwarding is disabled on this interface.


## -see-also




<a href="https://msdn.microsoft.com/1d161a7e-3ceb-429f-a41e-eccd7f98f084">PMGM_CREATION_ALERT_CALLBACK</a>
 

 

