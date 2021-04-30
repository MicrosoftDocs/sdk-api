---
UID: NE:mprapi._ROUTER_INTERFACE_TYPE
title: ROUTER_INTERFACE_TYPE (mprapi.h)
description: The ROUTER_INTERFACE_TYPE type enumerates the different kinds of interfaces on a router.
helpviewer_keywords: ["ROUTER_IF_TYPE_CLIENT","ROUTER_IF_TYPE_DEDICATED","ROUTER_IF_TYPE_DIALOUT","ROUTER_IF_TYPE_FULL_ROUTER","ROUTER_IF_TYPE_HOME_ROUTER","ROUTER_IF_TYPE_INTERNAL","ROUTER_IF_TYPE_LOOPBACK","ROUTER_INTERFACE_TYPE","ROUTER_INTERFACE_TYPE enumeration [RAS]","_mpr_router_interface_type","mprapi/ROUTER_IF_TYPE_CLIENT","mprapi/ROUTER_IF_TYPE_DEDICATED","mprapi/ROUTER_IF_TYPE_DIALOUT","mprapi/ROUTER_IF_TYPE_FULL_ROUTER","mprapi/ROUTER_IF_TYPE_HOME_ROUTER","mprapi/ROUTER_IF_TYPE_INTERNAL","mprapi/ROUTER_IF_TYPE_LOOPBACK","mprapi/ROUTER_INTERFACE_TYPE","rras.router_interface_type"]
old-location: rras\router_interface_type.htm
tech.root: RRAS
ms.assetid: 9b957ab0-0c5d-4478-914a-4837e6bbd56a
ms.date: 12/05/2018
ms.keywords: ROUTER_IF_TYPE_CLIENT, ROUTER_IF_TYPE_DEDICATED, ROUTER_IF_TYPE_DIALOUT, ROUTER_IF_TYPE_FULL_ROUTER, ROUTER_IF_TYPE_HOME_ROUTER, ROUTER_IF_TYPE_INTERNAL, ROUTER_IF_TYPE_LOOPBACK, ROUTER_INTERFACE_TYPE, ROUTER_INTERFACE_TYPE enumeration [RAS], _mpr_router_interface_type, mprapi/ROUTER_IF_TYPE_CLIENT, mprapi/ROUTER_IF_TYPE_DEDICATED, mprapi/ROUTER_IF_TYPE_DIALOUT, mprapi/ROUTER_IF_TYPE_FULL_ROUTER, mprapi/ROUTER_IF_TYPE_HOME_ROUTER, mprapi/ROUTER_IF_TYPE_INTERNAL, mprapi/ROUTER_IF_TYPE_LOOPBACK, mprapi/ROUTER_INTERFACE_TYPE, rras.router_interface_type
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
req.typenames: ROUTER_INTERFACE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ROUTER_INTERFACE_TYPE
 - mprapi/_ROUTER_INTERFACE_TYPE
 - ROUTER_INTERFACE_TYPE
 - mprapi/ROUTER_INTERFACE_TYPE
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
 - ROUTER_INTERFACE_TYPE
---

# ROUTER_INTERFACE_TYPE enumeration


## -description

The 
<b>ROUTER_INTERFACE_TYPE</b> type enumerates the different kinds of interfaces on a router.

## -enum-fields

### -field ROUTER_IF_TYPE_CLIENT

The interface is for a remote client.

### -field ROUTER_IF_TYPE_HOME_ROUTER

The interface is for a home router.

### -field ROUTER_IF_TYPE_FULL_ROUTER

The interface is for a full router.

### -field ROUTER_IF_TYPE_DEDICATED

The interface is always connected. It is a LAN interface, or the interface is connected over a leased line.

### -field ROUTER_IF_TYPE_INTERNAL

The interface is an internal-only interface.

### -field ROUTER_IF_TYPE_LOOPBACK

The interface is a loopback interface.

### -field ROUTER_IF_TYPE_TUNNEL1

### -field ROUTER_IF_TYPE_DIALOUT

The interface is a dial-on-demand (DOD) interface.

### -field ROUTER_IF_TYPE_MAX

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/RRAS/router-management-enumerations">Router Management Enumerated Types</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>