---
UID: NF:comsvcs.IMTSActivity.UnbindFromThread
title: IMTSActivity::UnbindFromThread (comsvcs.h)
description: Unbinds the batch work that is submitted using IMTSActivity::AsyncCall or IMTSActivity::SynchronousCall from the thread on which it is running.
helpviewer_keywords: ["IMTSActivity interface [COM+]","UnbindFromThread method","IMTSActivity.UnbindFromThread","IMTSActivity::UnbindFromThread","UnbindFromThread","UnbindFromThread method [COM+]","UnbindFromThread method [COM+]","IMTSActivity interface","_cos_IMTSActivity_UnbindFromThread","comsvcs/IMTSActivity::UnbindFromThread","cos.imtsactivity_unbindfromthread"]
old-location: cos\imtsactivity_unbindfromthread.htm
tech.root: cos
ms.assetid: cb4c4f63-2a6e-4df7-8886-19d45e28d81a
ms.date: 12/05/2018
ms.keywords: IMTSActivity interface [COM+],UnbindFromThread method, IMTSActivity.UnbindFromThread, IMTSActivity::UnbindFromThread, UnbindFromThread, UnbindFromThread method [COM+], UnbindFromThread method [COM+],IMTSActivity interface, _cos_IMTSActivity_UnbindFromThread, comsvcs/IMTSActivity::UnbindFromThread, cos.imtsactivity_unbindfromthread
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
 - IMTSActivity::UnbindFromThread
 - comsvcs/IMTSActivity::UnbindFromThread
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
 - IMTSActivity.UnbindFromThread
---

# IMTSActivity::UnbindFromThread


## -description

Unbinds the batch work that is submitted using <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">IMTSActivity::AsyncCall</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">IMTSActivity::SynchronousCall</a> from the thread on which it is running. It has no effect if the batch work was not previously bound to a thread.

This method is designed to be called from the implementation of the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtscall-oncall">IMTSCall::OnCall</a> method.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a>
