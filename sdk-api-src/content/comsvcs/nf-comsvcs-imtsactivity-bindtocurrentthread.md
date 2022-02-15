---
UID: NF:comsvcs.IMTSActivity.BindToCurrentThread
title: IMTSActivity::BindToCurrentThread (comsvcs.h)
description: Binds the batch work that is submitted using IMTSActivity::AsyncCall or IMTSActivity::SynchronousCall to the current single-threaded apartment (STA).
helpviewer_keywords: ["BindToCurrentThread","BindToCurrentThread method [COM+]","BindToCurrentThread method [COM+]","IMTSActivity interface","IMTSActivity interface [COM+]","BindToCurrentThread method","IMTSActivity.BindToCurrentThread","IMTSActivity::BindToCurrentThread","_cos_IMTSActivity_BindToCurrentThread","comsvcs/IMTSActivity::BindToCurrentThread","cos.imtsactivity_bindtocurrentthread"]
old-location: cos\imtsactivity_bindtocurrentthread.htm
tech.root: cos
ms.assetid: 31f0c64c-275c-431c-b85e-6ee5f4318e1f
ms.date: 12/05/2018
ms.keywords: BindToCurrentThread, BindToCurrentThread method [COM+], BindToCurrentThread method [COM+],IMTSActivity interface, IMTSActivity interface [COM+],BindToCurrentThread method, IMTSActivity.BindToCurrentThread, IMTSActivity::BindToCurrentThread, _cos_IMTSActivity_BindToCurrentThread, comsvcs/IMTSActivity::BindToCurrentThread, cos.imtsactivity_bindtocurrentthread
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
 - IMTSActivity::BindToCurrentThread
 - comsvcs/IMTSActivity::BindToCurrentThread
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
 - IMTSActivity.BindToCurrentThread
---

# IMTSActivity::BindToCurrentThread


## -description

Binds the batch work that is submitted using <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">IMTSActivity::AsyncCall</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">IMTSActivity::SynchronousCall</a> to the current single-threaded apartment (STA).

This method is designed to be called from the implementation of the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtscall-oncall">IMTSCall::OnCall</a> method.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a>
