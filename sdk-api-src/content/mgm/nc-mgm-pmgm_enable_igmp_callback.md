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

# PMGM_ENABLE_IGMP_CALLBACK callback function


## -description


The 
<b>PMGM_ENABLE_IGMP_CALLBACK</b> callback is a call into IGMP to notify it that a routing protocol has finished taking or releasing ownership of an interface.

When this callback is invoked, IGMP should add all its group memberships on the specified interface using calls to the 
<a href="https://msdn.microsoft.com/b767961e-0935-4662-9f54-d82dfa0e7bd0">MgmAddGroupMembershipEntry</a> function.


## -parameters




### -param dwIfIndex [in]

Specifies the index of the interface on which to enable IGMP.


### -param dwIfNextHopAddr [in]

Specifies the address of the next hop that corresponds to the index specified by <i>dwIfIndex</i>. The <i>dwIfIndex</i> and <i>dwIfNextHopIPAddr</i> parameters uniquely identify a next hop on point-to-multipoint interfaces. A point-to-multipoint interface is a connection where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple access (NBMA) interfaces and the internal interface on which all dial-up clients connect. 




For broadcast interfaces (such as Ethernet interfaces) or point-to-point interfaces, which are identified by only the value of <i>dwIfIndex</i>, specify zero.


## -returns



RRAS does not expect the application to return any specific value; any value returned is ignored by RRAS.





## -remarks



IGMP must not add group memberships in the context of this callback. The multicast group manager and IGMP  become deadlocked.




## -see-also




<a href="https://msdn.microsoft.com/4f790e1b-b10f-477b-b2bc-75c95560d7f4">PMGM_DISABLE_IGMP_CALLBACK</a>
 

 

