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

# _ROUTING_PROTOCOL_CONFIG structure


## -description


The 
<b>ROUTING_PROTOCOL_CONFIG</b> structure describes the routing protocol configuration information that is passed to the multicast group manager when a protocol registers with the multicast group manager.


## -struct-fields




### -field dwCallbackFlags

Reserved for future use.


### -field pfnRpfCallback

Callback into a routing protocol to perform an RPF check.


### -field pfnCreationAlertCallback

Callback into a routing protocol to determine the subset of interfaces owned by the routing protocol on which a multicast packet from a new source or to a new group should be forwarded.


### -field pfnPruneAlertCallback

Callback into a routing protocol to notify the protocol that receivers for the specified source and group are no longer present on an interface owned by other routing protocols.


### -field pfnJoinAlertCallback

Callback into a routing protocol to notify the protocol that new receivers for the specified source and group are present on an interface owned by another routing protocol.


### -field pfnWrongIfCallback

Callback into a routing protocol to notify the protocol that a packet has been received from the specified source and for the specified group on the wrong interface.


### -field pfnLocalJoinCallback

Callback into a routing protocol to notify the protocol that IGMP has detected new receivers for a group on an interface.


### -field pfnLocalLeaveCallback

Callback into a routing protocol to notify the protocol that IGMP has detected that there are no more receivers for a group on an interface.


### -field pfnDisableIgmpCallback

Callback into IGMP to notify IGMP that a protocol is taking or releasing ownership of an interface on which IGMP is enabled.


### -field pfnEnableIgmpCallback

Callback into IGMP to notify IGMP that a protocol has finished taking or releasing ownership of an interface on which IGMP is enabled.


## -see-also




<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>
 

 

