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

# ITuner::get_TuneRequest


## -description



The <b>get_TuneRequest</b> method gets the tune request currently in effect for the Network Provider.




## -parameters




### -param TuneRequest






#### - ppTuneRequest [out]

Address of an <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface pointer that will be set to the returned object.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



After a tune request is submitted to the Tuner, its Components collection will be filled in. By calling <b>get_TuneRequest</b> after tuning to the program, an application can determine which components are currently available for that program, and then use the <a href="https://msdn.microsoft.com/f1f9cf98-69fd-4c54-8023-742f86413220">IComponent::put_Status</a> method on the Component objects in the collection to activate or inactivate them. This is how an application, for example, changes from an English audio stream to a Spanish audio stream.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

