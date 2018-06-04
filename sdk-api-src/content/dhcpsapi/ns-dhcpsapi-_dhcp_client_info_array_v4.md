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

# _DHCP_CLIENT_INFO_ARRAY_V4 structure


## -description


The <b>DHCP_CLIENT_INFO_ARRAY_V4</b> structure defines an array of <a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structures for use with enumeration functions. 


## -struct-fields




### -field NumElements

Specifies the number of elements present in <b>Clients</b>.


### -field Clients

Pointer to a list of <a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a> structures that contain information on specific DHCP subnet clients, including the dynamic address type (DHCP and/or BOOTP).


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/ac058d7a-7257-4e40-8fc0-bc4ca107671b">DHCP_CLIENT_INFO_V4</a>
 

 

