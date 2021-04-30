---
UID: NS:mprapi._MPR_INTERFACE_0
title: MPR_INTERFACE_0 (mprapi.h)
description: The MPR_INTERFACE_0 structure contains information for a particular router interface.
helpviewer_keywords: ["*PMPR_INTERFACE_0","MPR_INTERFACE_0","MPR_INTERFACE_0 structure [RAS]","PMPR_INTERFACE_0","PMPR_INTERFACE_0 structure pointer [RAS]","_mpr_mpr_interface_0","mprapi/MPR_INTERFACE_0","mprapi/PMPR_INTERFACE_0","rras.mpr_interface_0"]
old-location: rras\mpr_interface_0.htm
tech.root: RRAS
ms.assetid: b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba
ms.date: 12/05/2018
ms.keywords: '*PMPR_INTERFACE_0, MPR_INTERFACE_0, MPR_INTERFACE_0 structure [RAS], PMPR_INTERFACE_0, PMPR_INTERFACE_0 structure pointer [RAS], _mpr_mpr_interface_0, mprapi/MPR_INTERFACE_0, mprapi/PMPR_INTERFACE_0, rras.mpr_interface_0'
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
req.typenames: MPR_INTERFACE_0, *PMPR_INTERFACE_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_INTERFACE_0
 - mprapi/_MPR_INTERFACE_0
 - PMPR_INTERFACE_0
 - mprapi/PMPR_INTERFACE_0
 - MPR_INTERFACE_0
 - mprapi/MPR_INTERFACE_0
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
 - MPR_INTERFACE_0
---

# MPR_INTERFACE_0 structure


## -description

The 
<b>MPR_INTERFACE_0</b> structure contains information for a particular router interface.

## -struct-fields

### -field wszInterfaceName

Pointer to a Unicode string that contains the name of the interface.

### -field hInterface

Handle to the interface.

### -field fEnabled

Specifies whether the interface is enabled. This member is <b>TRUE</b> if the interface is enabled, <b>FALSE</b> if the interface is administratively disabled.

### -field dwIfType

Specifies the 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">type of interface</a>.

### -field dwConnectionState

Specifies the current state of the interface, for example connected, disconnected, or unreachable. For a list of possible states, see 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a>.

### -field fUnReachabilityReasons

Specifies a value that represents a reason why the interface cannot be reached. See 
<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a> for a list of possible values.

### -field dwLastError

Specifies a nonzero value if the interface fails to connect.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a>



<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_INTERFACE_TYPE</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>



<a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a>