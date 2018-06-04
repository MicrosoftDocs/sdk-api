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

# IEventPublisher::PutDefaultProperty


## -description


Writes a named property and its value to the property bag associated with the event publisher.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be set.


### -param propertyValue [in]

The new value for the property.


## -returns



The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



An <a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.




## -see-also




<a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">IEventPublisher</a>
 

 

