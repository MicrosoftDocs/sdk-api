---
UID: NE:mprapi._ROUTER_CONNECTION_STATE
title: ROUTER_CONNECTION_STATE (mprapi.h)
description: Enumerates the possible states of an interface on a router.
helpviewer_keywords: ["ROUTER_CONNECTION_STATE","ROUTER_CONNECTION_STATE enumeration [RAS]","ROUTER_IF_STATE_CONNECTED","ROUTER_IF_STATE_CONNECTING","ROUTER_IF_STATE_DISCONNECTED","ROUTER_IF_STATE_UNREACHABLE","_mpr_router_connection_state","mprapi/ROUTER_CONNECTION_STATE","mprapi/ROUTER_IF_STATE_CONNECTED","mprapi/ROUTER_IF_STATE_CONNECTING","mprapi/ROUTER_IF_STATE_DISCONNECTED","mprapi/ROUTER_IF_STATE_UNREACHABLE","rras.router_connection_state"]
old-location: rras\router_connection_state.htm
tech.root: RRAS
ms.assetid: e98f9843-c5a2-4714-8e22-58f24256d08f
ms.date: 12/05/2018
ms.keywords: ROUTER_CONNECTION_STATE, ROUTER_CONNECTION_STATE enumeration [RAS], ROUTER_IF_STATE_CONNECTED, ROUTER_IF_STATE_CONNECTING, ROUTER_IF_STATE_DISCONNECTED, ROUTER_IF_STATE_UNREACHABLE, _mpr_router_connection_state, mprapi/ROUTER_CONNECTION_STATE, mprapi/ROUTER_IF_STATE_CONNECTED, mprapi/ROUTER_IF_STATE_CONNECTING, mprapi/ROUTER_IF_STATE_DISCONNECTED, mprapi/ROUTER_IF_STATE_UNREACHABLE, rras.router_connection_state
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
targetos: Windows
req.typenames: ROUTER_CONNECTION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ROUTER_CONNECTION_STATE
 - mprapi/_ROUTER_CONNECTION_STATE
 - ROUTER_CONNECTION_STATE
 - mprapi/ROUTER_CONNECTION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - ROUTER_CONNECTION_STATE
---

# ROUTER_CONNECTION_STATE enumeration


## -description

The 
<b>ROUTER_CONNECTION_STATE</b> type enumerates the possible states of an interface on a router.

## -enum-fields

### -field ROUTER_IF_STATE_UNREACHABLE

The interface is unreachable. For a list of possible reasons, see 
<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a>.

### -field ROUTER_IF_STATE_DISCONNECTED

The interface is reachable but disconnected.

### -field ROUTER_IF_STATE_CONNECTING

The interface is in the process of connecting.

### -field ROUTER_IF_STATE_CONNECTED

The interface is connected.

## -remarks

These states are sometimes referred to as <i>operational states</i>.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>



<a href="/windows/desktop/RRAS/router-management-enumerations">Router Management Enumerated Types</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a>