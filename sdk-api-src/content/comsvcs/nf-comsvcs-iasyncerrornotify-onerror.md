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

# IAsyncErrorNotify::OnError


## -description


Called by COM+ when an error occurs in your asynchronous batch work.


## -parameters




### -param hr [in]

The <b>HRESULT</b> value of the error that occurred while your batch work was running asynchronously.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



This method should be implemented to gracefully handle errors that occur when your batch work is running asynchronously. Because the process terminates (FailFast) on any unrecoverable error, without this method you have no way of knowing when errors occur in your asynchronous batch work. The process also terminates when this method returns an error as its return value.

The batch work itself is implemented in <a href="https://msdn.microsoft.com/0a2bb7ed-018f-4cb1-a1b2-27f6949dae39">IServiceCall::OnCall</a>, and it is run asynchronously by calling <a href="https://msdn.microsoft.com/1d81f2e6-9426-4733-bd1d-0b6ca087cc0a">IServiceActivity::AsynchronousCall</a> using the <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a> pointer that was returned from the call to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/870ab43a-c675-499b-a1e3-1f48176768c0">IAsyncErrorNotify</a>
 

 

