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

# _DHCP_CLIENT_SEARCH_TYPE enumeration


## -description



      The <b>DHCP_SEARCH_INFO_TYPE</b> enumeration defines the set of possible attributes used to search DHCP client information records.


## -enum-fields




### -field DhcpClientIpAddress

The search will be performed against the assigned DHCP client IP address, represented as a 32-bit unsigned integer value.


### -field DhcpClientHardwareAddress

The search will be performed against the MAC address of the DHCP client network interface device, represented as a <a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a> structure.


### -field DhcpClientName

The search will be performed against the DHCP client's network name, represented as a Unicode string.


## -see-also




<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a>



<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>
 

 

