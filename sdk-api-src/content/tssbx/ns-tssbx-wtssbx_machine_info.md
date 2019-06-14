---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0007
title: WTSSBX_MACHINE_INFO (tssbx.h)
author: windows-sdk-content
description: Contains information about a computer and its current state.
old-location: termserv\wtssbx_machine_info.htm
tech.root: TermServ
ms.assetid: 88d49ae4-bf48-4b04-8a16-58d32efd62fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSSBX_MACHINE_INFO, WTSSBX_MACHINE_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0007, termserv.wtssbx_machine_info, tssbx/WTSSBX_MACHINE_INFO
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tssbx.h
api_name:
 - WTSSBX_MACHINE_INFO
product: Windows
targetos: Windows
req.typenames: WTSSBX_MACHINE_INFO
req.redist: 
ms.custom: 19H1
---

# WTSSBX_MACHINE_INFO structure


## -description


Contains information about a computer and its current state.


## -struct-fields




### -field ClientConnectInfo

A <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/ns-tssbx-__midl_iwtssbplugin_0006">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the computer.


### -field wczFarmName

A Unicode string that contains the name of the farm in RD Connection Broker that this computer belongs to.  This string  cannot exceed 256 characters.


### -field InternalIPAddress

A <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/ns-tssbx-__midl_iwtssbplugin_0004">WTSSBX_IP_ADDRESS</a> structure that contains the internal IP address of this computer. RD Connection Broker uses this IP address for redirection purposes.


### -field dwMaxSessionsLimit

The maximum number of sessions that this computer can accept.


### -field ServerWeight

The server weight value of this computer. RD Connection Broker uses this value for load balancing.


### -field SingleSessionMode

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/ne-tssbx-__midl_iwtssbplugin_0002">WTSSBX_MACHINE_SESSION_MODE</a> enumeration type that indicates the computer's session mode.


### -field InDrain

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/ne-tssbx-__midl_iwtssbplugin_0001">WTSSBX_MACHINE_DRAIN</a> enumeration type that indicates whether the computer is accepting new user sessions.


### -field MachineState

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/tssbx/ne-tssbx-__midl_iwtssbplugin_0005">WTSSBX_MACHINE_STATE</a> enumeration type that indicates the state of the computer.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>
 

 

