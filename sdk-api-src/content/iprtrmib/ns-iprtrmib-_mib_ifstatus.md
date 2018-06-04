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

# _MIB_IFSTATUS structure


## -description


The 
<b>MIB_IFSTATUS</b> structure stores status information for a particular interface.


## -struct-fields




### -field dwIfIndex

The index that identifies the interface.


### -field dwAdminStatus

The administrative status of the interface, that is, whether the interface is administratively enabled or disabled.


### -field dwOperationalStatus

The operational status of the interface. This member can be one of the values defined in the <a href="https://msdn.microsoft.com/e98f9843-c5a2-4714-8e22-58f24256d08f">ROUTER_CONNECTION_STATE</a> enumeration defined in the <i>Mprapip.h</i> header file. See 
the <b>ROUTER_CONNECTION_STATE</b> enumeration for a list amd description of the possible operational states.


### -field bMHbeatActive

Specifies whether multicast heartbeat detection is enabled. A value of <b>TRUE</b> indicates that heartbeat detection is enabled. A value of <b>FALSE</b> indicates that heartbeat detection is disabled.


### -field bMHbeatAlive

Specifies whether the multicast heartbeat dead interval has been exceeded. A value of <b>FALSE</b> indicates that the interval has been exceeded. A value of <b>TRUE</b> indicates that the interval has not been exceeded.


## -remarks



Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>



<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>



<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>
 

 

