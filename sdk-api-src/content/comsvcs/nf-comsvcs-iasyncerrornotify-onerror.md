---
UID: NF:comsvcs.IAsyncErrorNotify.OnError
title: IAsyncErrorNotify::OnError method
author: windows-driver-content
description: Called by COM+ when an error occurs in your asynchronous batch work.
old-location: cos\iasyncerrornotify_onerror.htm
old-project: cossdk
ms.assetid: a48d7733-bbcb-4c03-b265-f112e24c07d9
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IAsyncErrorNotify, IAsyncErrorNotify interface [COM+], OnError method, IAsyncErrorNotify::OnError, OnError method [COM+], OnError method [COM+], IAsyncErrorNotify interface, OnError,IAsyncErrorNotify.OnError, _cos_IAsyncErrorNotify_OnError, comsvcs/IAsyncErrorNotify::OnError, cos.iasyncerrornotify_onerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IAsyncErrorNotify.OnError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAsyncErrorNotify::OnError method


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
 

 

