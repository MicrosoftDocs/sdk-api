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

# IF_OPER_STATUS enumeration


## -description


The <b>IF_OPER_STATUS</b> enumeration specifies the operational status of an interface.


## -enum-fields




### -field IfOperStatusUp

The interface is up and operational. The interface is able to pass packets.


### -field IfOperStatusDown

The interface is not down and not operational. The interface is unable to pass packets.


### -field IfOperStatusTesting

The interface is being tested.


### -field IfOperStatusUnknown

The interface status is unknown.


### -field IfOperStatusDormant

The interface is not
   in a condition to pass packets. The interface is  not up, but is
   in a pending state, waiting for some external event.  This state identifies the situation where the
   interface is waiting for events to place it in the up state.


### -field IfOperStatusNotPresent

This state is a refinement on the down state which
   indicates that the interface is down specifically because
   some component (for example, a hardware component) is not present in
   the system.


### -field IfOperStatusLowerLayerDown

This state is a refinement on the down state.
   The interface is operational, but a networking layer below the interface is not operational.


## -remarks



The <b>IF_OPER_STATUS</b> enumeration is used in the <b>OperStatus</b> member of the <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>  structure.




## -see-also




<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>
 

 

