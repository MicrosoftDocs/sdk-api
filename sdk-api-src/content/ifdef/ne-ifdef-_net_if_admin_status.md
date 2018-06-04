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

# _NET_IF_ADMIN_STATUS enumeration


## -description


The NET_IF_ADMIN_STATUS enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> administrative
  status, as described in RFC 2863.


## -enum-fields




### -field NET_IF_ADMIN_STATUS_UP

Specifies that the interface is initialized and enabled, but the interface is not necessarily
     ready to transmit and receive network data because that depends on the operational status of the
     interface. For more information about the operational status of an interface, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff569619">OID_GEN_OPERATIONAL_STATUS</a>.


### -field NET_IF_ADMIN_STATUS_DOWN

Specifies that the interface is down, and this interface cannot be used to transmit or receive
     network data.


### -field NET_IF_ADMIN_STATUS_TESTING

Specifies that the interface is in a test mode, and no network data can be transmitted or
     received.


## -remarks



For more information on RFC 2863, see 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=84054">"The Interfaces Group MIB"</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569437">OID_GEN_ADMIN_STATUS</a>
 

 

