---
UID: NF:comsvcs.IServiceActivity.UnbindFromThread
title: IServiceActivity::UnbindFromThread
author: windows-driver-content
description: Unbinds the user-defined batch work from the thread on which it is running.
old-location: cos\iserviceactivity_unbindfromthread.htm
old-project: cossdk
ms.assetid: e28b413d-6e3e-4a1f-90ed-8b0ab88904aa
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IServiceActivity interface [COM+],UnbindFromThread method, IServiceActivity.UnbindFromThread, IServiceActivity::UnbindFromThread, UnbindFromThread, UnbindFromThread method [COM+], UnbindFromThread method [COM+],IServiceActivity interface, _cos_IServiceActivity_UnbindFromThread, comsvcs/IServiceActivity::UnbindFromThread, cos.iserviceactivity_unbindfromthread
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
-	IServiceActivity.UnbindFromThread
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceActivity::UnbindFromThread


## -description


Unbinds the user-defined batch work from the thread on which it is running.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



This method unbinds the batch work that is submitted through the <a href="https://msdn.microsoft.com/1d81f2e6-9426-4733-bd1d-0b6ca087cc0a">AsynchronousCall</a> or the <a href="https://msdn.microsoft.com/d25e6942-7b1b-4b74-b711-2d0f513d0b38">SynchronousCall</a> method from the thread it is running on. It has no effect if the batch work was not previously bound to a thread.

Calling this method is equivalent to having called <a href="https://msdn.microsoft.com/9d2c4e6f-aa12-4874-a8e0-ca21a981b43f">IServiceThreadPoolConfig::SetBindingInfo</a> with CSC_NoBinding on the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that was passed through the <i>pIUnknown</i> parameter to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. However, after the activity has been created by <b>CoCreateActivity</b>, you can no longer call <b>IServiceThreadPoolConfig::SetBindingInfo</b> to change the thread binding. To change the thread binding after the activity has been created, you must call the <a href="https://msdn.microsoft.com/3d2b57fd-1714-4fdf-859c-9fdfb341dd5d">BindToCurrentThread</a> or the <b>UnbindFromThread</b> method of <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>
 

 

