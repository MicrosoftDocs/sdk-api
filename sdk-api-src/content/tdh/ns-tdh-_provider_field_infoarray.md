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

# _PROVIDER_FIELD_INFOARRAY structure


## -description



		Defines metadata information about the requested field.
		
		
	
	


## -struct-fields




### -field NumberOfElements

Number of elements in the <b>FieldInfoArray</b> array.


### -field FieldType

Type of field information in  the <b>FieldInfoArray</b> array. For possible values, see the <a href="https://msdn.microsoft.com/da525556-e42b-41cb-b954-300f378477e5">EVENT_FIELD_TYPE</a> enumeration. 


### -field FieldInfoArray

Array of <a href="https://msdn.microsoft.com/a7c88c25-3acc-42aa-bf2b-bc7651e84f8c">PROVIDER_FIELD_INFO</a> structures that define the field's name, description and value.


## -see-also




<a href="https://msdn.microsoft.com/ab34a433-b641-4408-81d5-c93609204d24">TdhEnumerateProviderFieldInformation</a>



<a href="https://msdn.microsoft.com/ca3c1519-0b86-4bdb-b027-9c662df5466e">TdhQueryProviderFieldInformation</a>
 

 

