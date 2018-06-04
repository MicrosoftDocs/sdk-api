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

# _DHCP_FORCE_FLAG enumeration


## -description



      The <b>DHCP_FORCE_FLAG</b> enumeration defines the set of flags describing the force level of a DHCP subnet element deletion operation.


## -enum-fields




### -field DhcpFullForce

The operation deletes all client records affected by the element, and then deletes the element.


### -field DhcpNoForce

The operation only deletes the subnet element, leaving intact any client records impacted by the change.


### -field DhcpFailoverForce

The operation deletes all client records affected by the element, and then deletes the element from the DHCP server. But it does not delete any registered DNS records associated with the deleted client records from the DNS server. This flag is only valid when passed to <a href="https://msdn.microsoft.com/e000a81b-b61b-4ba9-adee-4940edc78050">DhcpDeleteSubnet</a>. Note that the minimum server OS requirement for this value is Windows Server 2012 R2 with KB 3100473 installed.


## -see-also




<a href="https://msdn.microsoft.com/8232b2cc-0bb1-4509-ad5f-6d1d1ece9fe5">
        DhcpRemoveSubnetElementV5</a>
 

 

