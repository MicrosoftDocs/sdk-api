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

# _DHCP_MIB_INFO_V6 structure


## -description


The <b>DHCP_MIB_INFO_V6</b> structure contains statistics for the DHCPv6 server.


## -struct-fields




### -field Solicits

Integer value that specifies the number of DHCPSOLICIT messages received by the DHCPv6 server from DHCPv6 clients. 


### -field Advertises

Integer value that specifies the number of DHCPADVERTISE messages sent by DHCPv6 server to DHCPv6 clients.


### -field Requests

Integer value that specifies the number of DHCPREQUEST messages sent by DHCPv6 server to DHCPv6 clients.


### -field Renews

Integer value that specifies the number of DHCPRENEW messages sent by DHCPv6 server to DHCPv6 clients.


### -field Rebinds

Integer value that specifies the number of DHCPREBIND messages sent by DHCPv6 server to DHCPv6 clients.


### -field Replies

Integer value that specifies the number of DHCPREPLY messages sent by DHCPv6 server to DHCPv6 clients.


### -field Confirms

Integer value that specifies the number of DHCPCONFIRM messages sent by DHCPv6 server to DHCPv6 clients.


### -field Declines

Integer value that specifies the number of DHCPDECLINE messages sent by DHCPv6 server to DHCPv6 clients.


### -field Releases

Integer value that specifies the number of DHCPRELEASE messages sent by DHCPv6 server to DHCPv6 clients.


### -field Informs

Integer value that specifies the number of DHCPINFORM messages sent by DHCPv6 server to DHCPv6 clients.


### -field ServerStartTime


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> value that specifies the time the DHCPv6 server was started.


### -field Scopes

Integer value that contains the number of IPv6 scopes configured on the current DHCPv6 server. This member defines the number of DHCPv6 scopes in the subsequent member <b>ScopeInfo</b>.


### -field ScopeInfo

Pointer to an array of <a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a> structures that contain statistics on individual scopes defined on the DHCPv6 server.


### -field ScopeInfo.size_is

 


### -field ScopeInfo.size_is.Scopes

 




## -see-also




<a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a>
 

 

