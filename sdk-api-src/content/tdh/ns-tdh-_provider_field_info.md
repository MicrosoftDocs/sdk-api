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

# _PROVIDER_FIELD_INFO structure


## -description



		Defines the field information.
		
		
	
	


## -struct-fields




### -field NameOffset

Offset to the null-terminated Unicode string that contains the name of the field, in English only.


### -field DescriptionOffset

Offset to the null-terminated Unicode string that contains the localized description of the field. The value is zero if the description does not exist.


### -field Value

Field value.


## -see-also




<a href="https://msdn.microsoft.com/c3755ca2-7b17-4f86-9ae8-34621f8b8c1b">PROVIDER_FIELD_INFOARRAY</a>
 

 

