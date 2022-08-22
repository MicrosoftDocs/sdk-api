---
UID: NF:comsvcs.IServiceCall.OnCall
title: IServiceCall::OnCall (comsvcs.h)
description: Triggers the execution of the batch work implemented in this method. (IServiceCall.OnCall)
helpviewer_keywords: ["IServiceCall interface [COM+]","OnCall method","IServiceCall.OnCall","IServiceCall::OnCall","OnCall","OnCall method [COM+]","OnCall method [COM+]","IServiceCall interface","_cos_IServiceCall_OnCall","comsvcs/IServiceCall::OnCall","cos.iservicecall_oncall"]
old-location: cos\iservicecall_oncall.htm
tech.root: cos
ms.assetid: 0a2bb7ed-018f-4cb1-a1b2-27f6949dae39
ms.date: 12/05/2018
ms.keywords: IServiceCall interface [COM+],OnCall method, IServiceCall.OnCall, IServiceCall::OnCall, OnCall, OnCall method [COM+], OnCall method [COM+],IServiceCall interface, _cos_IServiceCall_OnCall, comsvcs/IServiceCall::OnCall, cos.iservicecall_oncall
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
 - IServiceCall::OnCall
 - comsvcs/IServiceCall::OnCall
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
 - IServiceCall.OnCall
---

# IServiceCall::OnCall


## -description

Triggers the execution of the batch work implemented in this method.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

The batch work that is run in this method runs in the context and thread apartment of the activity that was created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. The batch work in this method is run through a call to either <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-synchronouscall">SynchronousCall</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-asynchronouscall">AsynchronousCall</a>, using the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a> pointer that was returned from the call to <b>CoCreateActivity</b>.



You must make sure that this method is thread safe in situations where the activity object that is created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> is not created with a synchronized context because in such situations many calls to <b>OnCall</b> can run at the same time.



To achieve the best performance from the system, the context configuration of the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> should be matched to the batch work performed by the <b>OnCall</b> method. For example, if the batch work in the <b>OnCall</b> method uses poolable objects, the activity created by <b>CoCreateActivity</b> should be configured to use the multithreaded apartment (MTA).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>
