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

# _DHCP_SCAN_FLAG enumeration


## -description



      The <b>DHCP_SCAN_FLAG</b> enumeration defines the set of possible targets of synchronization during a database scan operation.


## -enum-fields




### -field DhcpRegistryFix

Indicates that the in-memory client lease cache on the DHCPv4 server does not contain the client lease IP address, but the DHCPv4 client lease database does contain it. (Note that this enumeration does not inform <a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a> to perform a registry operation despite the name.) Any reconciliation process should update the in-memory cache.


### -field DhcpDatabaseFix

Indicates that the client lease database on the DHCPv4 server does not contain the client lease IP address, but the in-memory cache of client leases  does contain it. Any reconciliation process should update the database.


## -see-also




<a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">
        DHCP_SCAN_ITEM</a>



<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
 

 

