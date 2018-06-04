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

# _DHCP_MIB_INFO_V5 structure


## -description


The <b>DHCP_MIB_INFO_V5</b> structure contains statistical information about a DHCP server.


## -struct-fields




### -field Discovers

The number of DISCOVER messages received by the DHCP server.


### -field Offers

The number of OFFER messages sent to DHCP clients.


### -field Requests

The number of REQUEST messages received by  DHCP clients.


### -field Acks

The number of ACK messages sent by the DHCP server.


### -field Naks

The number of NACK messages sent by the DHCP server.


### -field Declines

The number of DECLINE messages sent by DHCP clients.


### -field Releases

The number of RELEASE messages  received by the DHCP server.


### -field ServerStartTime


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> structure that contains the most recent time the DHCP server was started.


### -field QtnNumLeases

This member is not currently used. Please set this to value 0x00000000.


### -field QtnPctQtnLeases

This member is not currently used. Please set this to value 0x00000000.


### -field QtnProbationLeases

This member is not currently used. Please set this to value 0x00000000.


### -field QtnNonQtnLeases

This member is not currently used. Please set this to value 0x00000000.


### -field QtnExemptLeases

This member is not currently used. Please set this to value 0x00000000.


### -field QtnCapableClients

This member is not currently used. Please set this to value 0x00000000.


### -field QtnIASErrors

This member is not currently used. Please set this to value 0x00000000.


### -field DelayedOffers

The number of OFFER messages sent with a specific delay by the DHCP server.


### -field ScopesWithDelayedOffers

The number of scopes with a delay value greater than 0.


### -field Scopes

The total number of scopes configured on the DHCP server


### -field ScopeInfo

Pointer to a <a href="https://msdn.microsoft.com/5144d83e-f21e-4f68-bf33-c7245b31da01">SCOPE_MIB_INFO_V5</a> structure that contains specific information about the scopes configured on the DHCP server.


### -field ScopeInfo.size_is

 


### -field ScopeInfo.size_is.Scopes

 




## -see-also




<a href="https://msdn.microsoft.com/3439198d-5391-4f9b-a6fe-9a600e7dc77b">DhcpGetMibInfoV5</a>



<a href="https://msdn.microsoft.com/5144d83e-f21e-4f68-bf33-c7245b31da01">SCOPE_MIB_INFO_V5</a>
 

 

