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

# IMFSourceResolver::CancelObjectCreation


## -description



          Cancels an asynchronous request to create an object.
        


## -parameters




### -param pIUnknownCancelCookie






#### - ppIUnknownCancelCookie [in]


            Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/6e218b93-4855-40dd-96cc-c4ee02792c14">IMFSourceResolver::BeginCreateObjectFromByteStream</a> or <a href="https://msdn.microsoft.com/bc97c1fb-d23a-4887-b6ac-0751c254a405">IMFSourceResolver::BeginCreateObjectFromURL</a> method.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        You can use this method to cancel a previous call to <a href="https://msdn.microsoft.com/6e218b93-4855-40dd-96cc-c4ee02792c14">BeginCreateObjectFromByteStream</a> or <a href="https://msdn.microsoft.com/bc97c1fb-d23a-4887-b6ac-0751c254a405">BeginCreateObjectFromURL</a>. Because these methods are asynchronous, however, they might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.
      

<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

