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

# _DHCP_SCAN_LIST structure


## -description


The <b>DHCP_SCAN_LIST</b> structure defines a list of all desynchronized client lease IP address on a DHCPv4 server that must be fixed.


## -struct-fields




### -field NumScanItems

Specifies the number of <a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>
         structures listed in <i>ScanItems</i>.


### -field ScanItems

Pointer to a list of <a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>
         structures that contain the specific client IP addresses whose leases differed between the in-memory cache of client leases and the subnet client lease database during a <a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
       operation.


### -field ScanItems.size_is

 


### -field ScanItems.size_is.NumScanItems

 




## -see-also




<a href="https://msdn.microsoft.com/82e36660-fb56-4334-97d0-c34facad55a6">DHCP_SCAN_ITEM</a>



<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
 

 

