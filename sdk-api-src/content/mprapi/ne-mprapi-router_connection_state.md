---
UID: NE:mprapi._ROUTER_CONNECTION_STATE
title: ROUTER_CONNECTION_STATE (mprapi.h)
author: windows-sdk-content
description: Enumerates the possible states of an interface on a router.
old-location: rras\router_connection_state.htm
tech.root: RRAS
ms.assetid: e98f9843-c5a2-4714-8e22-58f24256d08f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ROUTER_CONNECTION_STATE, ROUTER_CONNECTION_STATE enumeration [RAS], ROUTER_IF_STATE_CONNECTED, ROUTER_IF_STATE_CONNECTING, ROUTER_IF_STATE_DISCONNECTED, ROUTER_IF_STATE_UNREACHABLE, _mpr_router_connection_state, mprapi/ROUTER_CONNECTION_STATE, mprapi/ROUTER_IF_STATE_CONNECTED, mprapi/ROUTER_IF_STATE_CONNECTING, mprapi/ROUTER_IF_STATE_DISCONNECTED, mprapi/ROUTER_IF_STATE_UNREACHABLE, rras.router_connection_state
ms.topic: enum
req.header: mprapi.h
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
 - Mprapi.h
api_name:
 - ROUTER_CONNECTION_STATE
product: Windows
targetos: Windows
req.typenames: ROUTER_CONNECTION_STATE
req.redist: 
---

# ROUTER_CONNECTION_STATE enumeration


## -description


The 
<b>ROUTER_CONNECTION_STATE</b> type enumerates the possible states of an interface on a router.


## -enum-fields




### -field ROUTER_IF_STATE_UNREACHABLE

The interface is unreachable. For a list of possible reasons, see 
<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a>.


### -field ROUTER_IF_STATE_DISCONNECTED

The interface is reachable but disconnected.


### -field ROUTER_IF_STATE_CONNECTING

The interface is in the process of connecting.


### -field ROUTER_IF_STATE_CONNECTED

The interface is connected.


## -remarks



These states are sometimes referred to as <i>operational states</i>.




## -see-also




<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>



<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>



<a href="https://msdn.microsoft.com/61265bb0-7884-4896-a76a-a2cc11ccccda">Router Management Enumerated Types</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a>
 

 

