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

# _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure


## -description


The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4</b> structure defines an array of subnet element data. Element data in the V4 structure contains client type information.


## -struct-fields




### -field NumElements

Specifies the number of elements in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/d17725da-516b-4be6-839e-9876653e63c4">DHCP_SUBNET_ELEMENT_DATA_V4</a> structures that contain the data for the corresponding subnet elements.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/d17725da-516b-4be6-839e-9876653e63c4">DHCP_SUBNET_ELEMENT_DATA_V4</a>



<a href="https://msdn.microsoft.com/561a7aac-eed9-4a80-a4a4-f3a7727ae92a">DhcpEnumSubnetElementsV4</a>
 

 

