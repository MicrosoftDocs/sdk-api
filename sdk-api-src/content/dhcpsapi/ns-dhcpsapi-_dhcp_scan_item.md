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

# _DHCP_SCAN_ITEM structure


## -description


The <b>DHCP_SCAN_ITEM</b> structure defines a desynchronized client lease address stored on a DHCPv4 server, and the location in which it should be fixed (in-memory cache or database).


## -struct-fields




### -field IpAddress

DHCP_IP_ADDRESS value that specifies the address whose lease status was changed during a scan operation.


### -field ScanFlag


<a href="https://msdn.microsoft.com/825a0e64-b0c2-453e-8e00-52f84c40bef3">DHCP_SCAN_FLAG</a>
         enumeration value that indicates whether the supplied client lease IP address will be fixed in the DHCPv4 server's  in-memory client lease cache or the client lease database proper.


## -see-also




<a href="https://msdn.microsoft.com/825a0e64-b0c2-453e-8e00-52f84c40bef3">DHCP_SCAN_FLAG</a>



<a href="https://msdn.microsoft.com/9dc20612-1c08-4493-aab3-b524d8d88251">DHCP_SCAN_LIST</a>



<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>
 

 

