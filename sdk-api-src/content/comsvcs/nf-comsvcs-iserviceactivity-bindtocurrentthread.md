---
UID: NF:comsvcs.IServiceActivity.BindToCurrentThread
title: IServiceActivity::BindToCurrentThread
author: windows-sdk-content
description: Binds the user-defined batch work to the current thread.
old-location: cos\iserviceactivity_bindtocurrentthread.htm
tech.root: cossdk
ms.assetid: 3d2b57fd-1714-4fdf-859c-9fdfb341dd5d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BindToCurrentThread, BindToCurrentThread method [COM+], BindToCurrentThread method [COM+],IServiceActivity interface, IServiceActivity interface [COM+],BindToCurrentThread method, IServiceActivity.BindToCurrentThread, IServiceActivity::BindToCurrentThread, _cos_IServiceActivity_BindToCurrentThread, comsvcs/IServiceActivity::BindToCurrentThread, cos.iserviceactivity_bindtocurrentthread
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
 - IServiceActivity.BindToCurrentThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IServiceActivity.BindToCurrentThread
: 
---

# IServiceActivity::BindToCurrentThread


## -description


Binds the user-defined batch work to the current thread.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



This method binds the batch work that is submitted via the AsynchronousCall or the SynchronousCall method to the current single-threaded apartment (STA). It has no effect if the current thread is being run in the multithreaded apartment (MTA). The current thread model is determined by the configuration of the <a href="https://msdn.microsoft.com/en-us/library/ms683642(v=VS.85).aspx">IServiceThreadPoolConfig</a> interface of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that is passed via the <i>pIUnknown</i> parameter during the call to <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>.



Calling this method is equivalent to having called <a href="https://msdn.microsoft.com/en-us/library/ms684962(v=VS.85).aspx">IServiceThreadPoolConfig::SetBindingInfo</a> with CSC_BindToPoolThread on the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that was passed through the <i>pIUnknown</i> parameter to <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>. However, after the activity has been created by <b>CoCreateActivity</b>, you can no longer call <b>IServiceThreadPoolConfig::SetBindingInfo</b> to change the thread binding. To change the thread binding after the activity has been created, you must call the <b>BindToCurrentThread</b> or the <a href="https://msdn.microsoft.com/en-us/library/ms687124(v=VS.85).aspx">UnbindFromThread</a> method of <a href="https://msdn.microsoft.com/en-us/library/ms678822(v=VS.85).aspx">IServiceActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms678822(v=VS.85).aspx">IServiceActivity</a>
 

 

