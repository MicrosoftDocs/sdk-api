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

# SafeRef function


## -description


<p class="CCE_Message">[Do not use SafeRef in COM+. This function was used by objects in MTS to obtain a reference to itself. With COM+, this is no longer necessary.]


## -parameters




### -param rid [in]

A reference to the IID of the interface that the current object wants to pass to another object or client.


### -param pUnk [in]

A reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the current object.


## -returns



If the function succeds, the return value is a pointer to the specified interface that can be passed outside the current object's context. Otherwise, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/1ecc5a8e-58d8-42e7-a543-da86ad966983">IMTxAS::SafeRef</a>
 

 

