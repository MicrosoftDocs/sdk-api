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

# _QuarantineStatus enumeration


## -description


The <b>QuarantineStatus</b> enumeration specifies possible health status values for the DHCPv4 client, as validated at the NAP server.



## -enum-fields




### -field NOQUARANTINE

The DHCP client is compliant with the health policies defined by the administrator and has normal access to the network.


### -field RESTRICTEDACCESS

The DHCP client is not compliant with the health policies defined by the administrator and is being quarantined with restricted access to the network.


### -field DROPPACKET

The DHCP client is not compliant with the health policies defined by the administrator and is being denied access to the network. The DHCP server does not grant an IP address lease to this client.


### -field PROBATION

The DHCP client is not compliant with the health policies defined by the administrator and is being granted normal access to the network for a limited time.


### -field EXEMPT

The DHCP client is exempt from compliance with the health policies defined by the administrator and is granted normal access to the network.


### -field DEFAULTQUARSETTING

The DHCP client is put into the default quarantine state configured on the DHCP NAP server. When a network policy server (NPS) is unavailable, the DHCP client can be put in any of the states NOQUARANTINE, RESTRICTEDACCESS, or DROPPACKET, depending on the default setting on the DHCP NAP server.


### -field NOQUARINFO

No quarantine.


## -remarks



The <b>QuarantineStatus</b> enumeration is used in the <a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a>, <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a>, <a href="https://msdn.microsoft.com/3ee224fb-650f-4468-848b-960424202ac3">DHCP_CLIENT_INFO_PB</a>, and <a href="https://msdn.microsoft.com/46e4fb62-5b8e-44f8-b3a0-92535ca690f0">DHCPV4_FAILOVER_CLIENT_INFO</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/46e4fb62-5b8e-44f8-b3a0-92535ca690f0">DHCPV4_FAILOVER_CLIENT_INFO</a>



<a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a>



<a href="https://msdn.microsoft.com/3ee224fb-650f-4468-848b-960424202ac3">DHCP_CLIENT_INFO_PB</a>



<a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a>
 

 

