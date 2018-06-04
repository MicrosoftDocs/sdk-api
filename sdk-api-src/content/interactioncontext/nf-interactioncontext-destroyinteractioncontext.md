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

# DestroyInteractionContext function


## -description


Destroys the specified <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>DestroyInteractionContext</b> must be called to destroy any interaction context created by <a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/5c9b7756-fad1-4656-952c-78845685aa21">ResetInteractionContext</a>



<a href="https://msdn.microsoft.com/52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b">StopInteractionContext</a>
 

 

