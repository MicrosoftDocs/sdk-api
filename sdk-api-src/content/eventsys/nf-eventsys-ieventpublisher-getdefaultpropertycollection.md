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

# IEventPublisher::GetDefaultPropertyCollection


## -description


Creates a collection object that enumerates the properties contained in the property bag associated with the event publisher object.


## -parameters




### -param collection [out, retval]

A pointer to an <a href="_cos_IEventObjectCollection">IEventObjectCollection</a> interface pointer on an event object collection. This parameter cannot be <b>NULL</b>.


## -returns



The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



An <a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.




## -see-also




<a href="https://msdn.microsoft.com/132b79c8-d7f4-49c1-87c7-9bdf311ae697">IEventPublisher</a>
 

 

