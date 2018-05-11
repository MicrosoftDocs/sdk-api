---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0007
title: "__MIDL_IWTSSBPlugin_0007"
author: windows-driver-content
description: Contains information about a computer and its current state.
old-location: termserv\wtssbx_machine_info.htm
old-project: TermServ
ms.assetid: 88d49ae4-bf48-4b04-8a16-58d32efd62fa
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: WTSSBX_MACHINE_INFO, WTSSBX_MACHINE_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0007, termserv.wtssbx_machine_info, tssbx/WTSSBX_MACHINE_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSSBX_MACHINE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tssbx.h
api_name:
-	WTSSBX_MACHINE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

