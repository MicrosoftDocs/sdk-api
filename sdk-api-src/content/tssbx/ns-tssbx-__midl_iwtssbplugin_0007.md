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

# __MIDL_IWTSSBPlugin_0007 structure


## -description


Contains information about a computer and its current state.


## -struct-fields




### -field ClientConnectInfo

A <a href="https://msdn.microsoft.com/805e606b-6f30-4f49-af04-b7f298c4fadf">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the computer.


### -field wczFarmName

A Unicode string that contains the name of the farm in RD Connection Broker that this computer belongs to.  This string  cannot exceed 256 characters.


### -field InternalIPAddress

A <a href="https://msdn.microsoft.com/92fe662a-ad31-4ed3-9393-c7d86f97e702">WTSSBX_IP_ADDRESS</a> structure that contains the internal IP address of this computer. RD Connection Broker uses this IP address for redirection purposes.


### -field dwMaxSessionsLimit

The maximum number of sessions that this computer can accept.


### -field ServerWeight

The server weight value of this computer. RD Connection Broker uses this value for load balancing.


### -field SingleSessionMode

A value of the <a href="https://msdn.microsoft.com/38894819-a39f-4c1f-aef9-ec3036b42877">WTSSBX_MACHINE_SESSION_MODE</a> enumeration type that indicates the computer's session mode.


### -field InDrain

A value of the <a href="https://msdn.microsoft.com/251d1534-0571-427a-a9a1-2327eba55c2d">WTSSBX_MACHINE_DRAIN</a> enumeration type that indicates whether the computer is accepting new user sessions.


### -field MachineState

A value of the <a href="https://msdn.microsoft.com/8913e159-9b97-4575-9718-6f2906896a32">WTSSBX_MACHINE_STATE</a> enumeration type that indicates the state of the computer.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

