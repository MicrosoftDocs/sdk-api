---
UID: NF:comsvcs.IMTSCall.OnCall
title: IMTSCall::OnCall (comsvcs.h)
description: Triggers the execution of the batch work implemented in this method. (IMTSCall.OnCall)
helpviewer_keywords: ["IMTSCall interface [COM+]","OnCall method","IMTSCall.OnCall","IMTSCall::OnCall","OnCall","OnCall method [COM+]","OnCall method [COM+]","IMTSCall interface","_cos_IMTSCall_OnCall","comsvcs/IMTSCall::OnCall","cos.imtscall_oncall"]
old-location: cos\imtscall_oncall.htm
tech.root: cos
ms.assetid: 410ed66e-db55-41e6-8f09-df4fe3aad3f2
ms.date: 12/05/2018
ms.keywords: IMTSCall interface [COM+],OnCall method, IMTSCall.OnCall, IMTSCall::OnCall, OnCall, OnCall method [COM+], OnCall method [COM+],IMTSCall interface, _cos_IMTSCall_OnCall, comsvcs/IMTSCall::OnCall, cos.imtscall_oncall
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMTSCall::OnCall
 - comsvcs/IMTSCall::OnCall
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
 - IMTSCall.OnCall
---

# IMTSCall::OnCall


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtscall">IMTSCall</a> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>.]

Triggers the execution of the batch work implemented in this method.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The batch work that is run in this method runs in the context and thread apartment of the activity that was created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a>. The batch work in this method is run using a call to either <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">IMTSActivity::SynchronousCall</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">IMTSActivity::AsyncCall</a>, using the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a> pointer that was returned from the call to <b>MTSCreateActivity</b>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtscall">IMTSCall</a>
