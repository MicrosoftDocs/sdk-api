---
UID: NF:comsvcs.IServiceActivity.BindToCurrentThread
title: IServiceActivity::BindToCurrentThread (comsvcs.h)
description: Binds the user-defined batch work to the current thread.
helpviewer_keywords: ["BindToCurrentThread","BindToCurrentThread method [COM+]","BindToCurrentThread method [COM+]","IServiceActivity interface","IServiceActivity interface [COM+]","BindToCurrentThread method","IServiceActivity.BindToCurrentThread","IServiceActivity::BindToCurrentThread","_cos_IServiceActivity_BindToCurrentThread","comsvcs/IServiceActivity::BindToCurrentThread","cos.iserviceactivity_bindtocurrentthread"]
old-location: cos\iserviceactivity_bindtocurrentthread.htm
tech.root: cos
ms.assetid: 3d2b57fd-1714-4fdf-859c-9fdfb341dd5d
ms.date: 12/05/2018
ms.keywords: BindToCurrentThread, BindToCurrentThread method [COM+], BindToCurrentThread method [COM+],IServiceActivity interface, IServiceActivity interface [COM+],BindToCurrentThread method, IServiceActivity.BindToCurrentThread, IServiceActivity::BindToCurrentThread, _cos_IServiceActivity_BindToCurrentThread, comsvcs/IServiceActivity::BindToCurrentThread, cos.iserviceactivity_bindtocurrentthread
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceActivity::BindToCurrentThread
 - comsvcs/IServiceActivity::BindToCurrentThread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceActivity.BindToCurrentThread
---

# IServiceActivity::BindToCurrentThread


## -description

Binds the user-defined batch work to the current thread.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

This method binds the batch work that is submitted via the AsynchronousCall or the SynchronousCall method to the current single-threaded apartment (STA). It has no effect if the current thread is being run in the multithreaded apartment (MTA). The current thread model is determined by the configuration of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicethreadpoolconfig">IServiceThreadPoolConfig</a> interface of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that is passed via the <i>pIUnknown</i> parameter during the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.



Calling this method is equivalent to having called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-setbindinginfo">IServiceThreadPoolConfig::SetBindingInfo</a> with CSC_BindToPoolThread on the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that was passed through the <i>pIUnknown</i> parameter to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. However, after the activity has been created by <b>CoCreateActivity</b>, you can no longer call <b>IServiceThreadPoolConfig::SetBindingInfo</b> to change the thread binding. To change the thread binding after the activity has been created, you must call the <b>BindToCurrentThread</b> or the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-unbindfromthread">UnbindFromThread</a> method of <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>
