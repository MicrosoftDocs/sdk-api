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

# ISynchronizeHandle::GetHandle


## -description


Retrieves a handle to the synchronization object.


## -parameters




### -param ph [out]

A pointer to the variable that receives a handle to the synchronization object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e278930c-4f4d-4ac5-ba1e-a4a84bfcd0ca">ISynchronizeEvent::SetEventHandle</a>



<a href="https://msdn.microsoft.com/93b2e682-78da-4a61-a045-8d71b3834e1d">ISynchronizeHandle</a>
 

 

