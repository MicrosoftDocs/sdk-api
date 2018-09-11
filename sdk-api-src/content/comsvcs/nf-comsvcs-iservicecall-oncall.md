---
UID: NF:comsvcs.IServiceCall.OnCall
title: IServiceCall::OnCall
author: windows-sdk-content
description: Triggers the execution of the batch work implemented in this method.
old-location: cos\iservicecall_oncall.htm
tech.root: cossdk
ms.assetid: 0a2bb7ed-018f-4cb1-a1b2-27f6949dae39
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IServiceCall interface [COM+],OnCall method, IServiceCall.OnCall, IServiceCall::OnCall, OnCall, OnCall method [COM+], OnCall method [COM+],IServiceCall interface, _cos_IServiceCall_OnCall, comsvcs/IServiceCall::OnCall, cos.iservicecall_oncall
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceCall.OnCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceCall::OnCall


## -description


Triggers the execution of the batch work implemented in this method.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The batch work that is run in this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. The batch work in this method is run through a call to either <a href="https://msdn.microsoft.com/d25e6942-7b1b-4b74-b711-2d0f513d0b38">SynchronousCall</a> or <a href="https://msdn.microsoft.com/1d81f2e6-9426-4733-bd1d-0b6ca087cc0a">AsynchronousCall</a>, using the <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a> pointer that was returned from the call to <b>CoCreateActivity</b>.



You must make sure that this method is thread safe in situations where the activity object that is created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> is not created with a synchronized context because in such situations many calls to <b>OnCall</b> can run at the same time.



To achieve the best performance from the system, the context configuration of the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> should be matched to the batch work performed by the <b>OnCall</b> method. For example, if the batch work in the <b>OnCall</b> method uses poolable objects, the activity created by <b>CoCreateActivity</b> should be configured to use the multithreaded apartment (MTA).





## -see-also




<a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>
 

 

