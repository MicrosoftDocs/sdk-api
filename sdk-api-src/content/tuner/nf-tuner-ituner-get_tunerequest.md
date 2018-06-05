---
UID: NF:tuner.ITuner.get_TuneRequest
title: ITuner::get_TuneRequest
author: windows-sdk-content
description: The get_TuneRequest method gets the tune request currently in effect for the Network Provider.
old-location: mstv\ituner_get_tunerequest.htm
old-project: mstv
ms.assetid: 45967073-2e09-4490-967f-4ed3c9ed1d7e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_TuneRequest method, ITuner.get_TuneRequest, ITuner::get_TuneRequest, ITunerget_TuneRequest, get_TuneRequest, get_TuneRequest method [Microsoft TV Technologies], get_TuneRequest method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_tunerequest, tuner/ITuner::get_TuneRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuner.get_TuneRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

