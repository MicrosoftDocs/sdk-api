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
 

 

