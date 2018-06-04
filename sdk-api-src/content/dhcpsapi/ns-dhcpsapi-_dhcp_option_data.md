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

# _DHCP_OPTION_DATA structure


## -description


The <b>DHCP_OPTION_DATA</b> structure defines a data container for one or more data elements associated with a DHCP option.


## -struct-fields




### -field NumElements

Specifies the number of option data elements listed in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/2ffc8968-f903-4d8e-8b34-c8031a56ebfc">DHCP_OPTION_DATA_ELEMENT</a> structures that contain the data elements associated with this particular option element.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/2ffc8968-f903-4d8e-8b34-c8031a56ebfc">DHCP_OPTION_DATA_ELEMENT</a>
 

 

