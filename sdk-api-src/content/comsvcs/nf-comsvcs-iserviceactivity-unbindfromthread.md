---
UID: NF:comsvcs.IServiceActivity.UnbindFromThread
title: IServiceActivity::UnbindFromThread (comsvcs.h)
author: windows-sdk-content
description: Unbinds the user-defined batch work from the thread on which it is running.
old-location: cos\iserviceactivity_unbindfromthread.htm
tech.root: cossdk
ms.assetid: e28b413d-6e3e-4a1f-90ed-8b0ab88904aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IServiceActivity interface [COM+],UnbindFromThread method, IServiceActivity.UnbindFromThread, IServiceActivity::UnbindFromThread, UnbindFromThread, UnbindFromThread method [COM+], UnbindFromThread method [COM+],IServiceActivity interface, _cos_IServiceActivity_UnbindFromThread, comsvcs/IServiceActivity::UnbindFromThread, cos.iserviceactivity_unbindfromthread
ms.topic: method
f1_keywords: 
 - "comsvcs/IServiceActivity.UnbindFromThread"
dev_langs:
 - c++
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
 - IServiceActivity.UnbindFromThread
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceActivity::UnbindFromThread


## -description


Unbinds the user-defined batch work from the thread on which it is running.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



This method unbinds the batch work that is submitted through the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-asynchronouscall">AsynchronousCall</a> or the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-synchronouscall">SynchronousCall</a> method from the thread it is running on. It has no effect if the batch work was not previously bound to a thread.

Calling this method is equivalent to having called <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-setbindinginfo">IServiceThreadPoolConfig::SetBindingInfo</a> with CSC_NoBinding on the <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that was passed through the <i>pIUnknown</i> parameter to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. However, after the activity has been created by <b>CoCreateActivity</b>, you can no longer call <b>IServiceThreadPoolConfig::SetBindingInfo</b> to change the thread binding. To change the thread binding after the activity has been created, you must call the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-bindtocurrentthread">BindToCurrentThread</a> or the <b>UnbindFromThread</b> method of <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>
 

 

