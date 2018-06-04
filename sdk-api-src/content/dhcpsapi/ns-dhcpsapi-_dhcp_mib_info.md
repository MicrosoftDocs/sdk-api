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

# _DHCP_MIB_INFO structure


## -description


The <b>DHCP_MIB_INFO</b> structure defines information returned from the DHCP-specific SNMP Management Information Block (MIB) about the current DHCP service.


## -struct-fields




### -field Discovers

Contains the number of DHCP discovery messages received.


### -field Offers

Contains the number of DHCP service offer messages transmitted.


### -field Requests

Contains the number of dynamic address request messages received.


### -field Acks

Contains the number of DHCP ACK messages received.


### -field Naks

Contains the number of DHCP NACK messages received.


### -field Declines

Contains the number of dynamic address service decline messages received.


### -field Releases

Contains the number of dynamic address release messages received.


### -field ServerStartTime


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> structure that contains the date and time the DHCP service started.


### -field Scopes

Contains the number of scopes defined on the DHCP server.


### -field ScopeInfo

Array of <a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a> structures that contain information on each subnet defined on the server. There are exactly <b>Scopes</b> elements in this array. If no subnets are defined (<b>Scopes</b> is 0), this field will be <b>NULL</b>.


### -field ScopeInfo.size_is

 


### -field ScopeInfo.size_is.Scopes

 




## -see-also




<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>



<a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a>
 

 

