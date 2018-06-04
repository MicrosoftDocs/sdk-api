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

# _DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure


## -description


The <b>DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY</b> structure contains an array of information elements for DHCPv4 clients.




## -struct-fields




### -field NumElements

Integer value that contains the number of DHCPv4 clients in the subsequent field Clients.



### -field Clients

Pointer to an array of  <a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a> structures that contain the DHCPv4 clients'  information.




### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a>
 

 

