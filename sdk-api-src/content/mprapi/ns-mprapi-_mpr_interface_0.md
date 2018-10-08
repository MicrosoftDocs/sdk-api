---
UID: NS:mprapi._MPR_INTERFACE_0
title: "_MPR_INTERFACE_0"
author: windows-sdk-content
description: The MPR_INTERFACE_0 structure contains information for a particular router interface.
old-location: rras\mpr_interface_0.htm
tech.root: rras
ms.assetid: b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PMPR_INTERFACE_0, MPR_INTERFACE_0, MPR_INTERFACE_0 structure [RAS], PMPR_INTERFACE_0, PMPR_INTERFACE_0 structure pointer [RAS], _MPR_INTERFACE_0, _mpr_mpr_interface_0, mprapi/MPR_INTERFACE_0, mprapi/PMPR_INTERFACE_0, rras.mpr_interface_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - MPR_INTERFACE_0
product: Windows
targetos: Windows
req.typenames: MPR_INTERFACE_0, *PMPR_INTERFACE_0
req.redist: 
---

# _MPR_INTERFACE_0 structure


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
<a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">type of interface</a>.


### -field dwConnectionState

Specifies the current state of the interface, for example connected, disconnected, or unreachable. For a list of possible states, see 
<a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a>.


### -field fUnReachabilityReasons

Specifies a value that represents a reason why the interface cannot be reached. See 
<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a> for a list of possible values.


### -field dwLastError

Specifies a nonzero value if the interface fails to connect.


## -see-also




<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>



<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a>



<a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>



<a href="https://msdn.microsoft.com/55c0519e-02c8-4a04-bed9-9fe94327a4b6">Unreachability Reasons</a>
 

 

