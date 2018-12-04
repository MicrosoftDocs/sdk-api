---
UID: NS:mgm._ROUTING_PROTOCOL_CONFIG
title: "_ROUTING_PROTOCOL_CONFIG"
author: windows-sdk-content
description: The ROUTING_PROTOCOL_CONFIG structure describes the routing protocol configuration information that is passed to the multicast group manager when a protocol registers with the multicast group manager.
old-location: rras\routing_protocol_config_str.htm
tech.root: rras
ms.assetid: acbf0519-a0c8-4b96-9722-9eeccee026d7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PROUTING_PROTOCOL_CONFIG, PROUTING_PROTOCOL_CONFIG, PROUTING_PROTOCOL_CONFIG structure pointer [RAS], ROUTING_PROTOCOL_CONFIG, ROUTING_PROTOCOL_CONFIG structure [RAS], _ROUTING_PROTOCOL_CONFIG, _mpr_routing_protocol_config_str, mgm/PROUTING_PROTOCOL_CONFIG, mgm/ROUTING_PROTOCOL_CONFIG, rras.routing_protocol_config_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - ROUTING_PROTOCOL_CONFIG
product: Windows
targetos: Windows
req.typenames: ROUTING_PROTOCOL_CONFIG, *PROUTING_PROTOCOL_CONFIG
req.redist: 
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
 

 

