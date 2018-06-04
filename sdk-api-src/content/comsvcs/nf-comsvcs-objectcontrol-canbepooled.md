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

# ObjectControl::CanBePooled


## -description


Indicates whether the object can be pooled for reuse when it is deactivated.


## -parameters




### -param pbPoolable [out]

Indicates whether the COM+ run-time environment can pool this object on deactivation for later reuse.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



When an object returns <b>TRUE</b> from <b>CanBePooled</b>, it indicates to the COM+ run-time environment that it can be added to an object pool after deactivation rather than being destroyed. Whenever an instance is required, one is drawn from the pool rather than being created.

Returning <b>TRUE</b> from <b>CanBePooled</b> does not guarantee that objects will be recycled; it only gives the COM+ run-time environment permission to recycle them. Returning <b>FALSE</b> from the <b>CanBePooled</b> method guarantees that instances of a component are not recycled.

The <a href="https://msdn.microsoft.com/70b260e7-a51d-4ddc-b395-5478e368e776">Activate</a> method is called if a new instance is created or if a recycled instance is drawn from the pool. Similarly, the <a href="https://msdn.microsoft.com/86ab7f50-6f2e-4c6c-ba4d-fd302cccf97d">Deactivate</a> method is called every time the object is deactivated, whether it is being destroyed or returned to the pool for recycling.




## -see-also




<a href="https://msdn.microsoft.com/954cf9ee-e76c-4faf-99aa-3648a7bb8a59">COM+ Object Pooling</a>



<a href="https://msdn.microsoft.com/34978b50-cd20-42fd-ad46-410190478ef8">How Object Pooling Works</a>



<a href="https://msdn.microsoft.com/3ca939de-31ce-4ce6-84cd-4b4191a0753c">ObjectControl</a>



<a href="https://msdn.microsoft.com/2cd4211e-be12-4197-8b43-5cb9f2321016">Requirements for Poolable Objects</a>
 

 

