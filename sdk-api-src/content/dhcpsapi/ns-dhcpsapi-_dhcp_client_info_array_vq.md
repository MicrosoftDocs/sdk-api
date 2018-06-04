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

# _DHCP_CLIENT_INFO_ARRAY_VQ structure


## -description


The <b>DHCP_CLIENT_INFO_ARRAY_VQ</b> structure specifies an array of <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structures.


## -struct-fields




### -field NumElements

The number of elements in the array.


### -field Clients

Pointer to the first element in the array of <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structures.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a>
 

 

