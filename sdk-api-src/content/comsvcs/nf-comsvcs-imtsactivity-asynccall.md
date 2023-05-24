---
UID: NF:comsvcs.IMTSActivity.AsyncCall
title: IMTSActivity::AsyncCall (comsvcs.h)
description: Performs the user-defined work asynchronously. (IMTSActivity.AsyncCall)
helpviewer_keywords: ["AsyncCall","AsyncCall method [COM+]","AsyncCall method [COM+]","IMTSActivity interface","IMTSActivity interface [COM+]","AsyncCall method","IMTSActivity.AsyncCall","IMTSActivity::AsyncCall","_cos_IMTSActivity_AsyncCall","comsvcs/IMTSActivity::AsyncCall","cos.imtsactivity_asynccall"]
old-location: cos\imtsactivity_asynccall.htm
tech.root: cos
ms.assetid: ccbb96e8-9fb8-40b4-b027-432ba8c400c7
ms.date: 12/05/2018
ms.keywords: AsyncCall, AsyncCall method [COM+], AsyncCall method [COM+],IMTSActivity interface, IMTSActivity interface [COM+],AsyncCall method, IMTSActivity.AsyncCall, IMTSActivity::AsyncCall, _cos_IMTSActivity_AsyncCall, comsvcs/IMTSActivity::AsyncCall, cos.imtsactivity_asynccall
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
 - IMTSActivity::AsyncCall
 - comsvcs/IMTSActivity::AsyncCall
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
 - IMTSActivity.AsyncCall
---

# IMTSActivity::AsyncCall


## -description

Performs the user-defined work asynchronously.

## -parameters

### -param pCall [in]

A pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtscall">IMTSCall</a> interface that is used to implement the batch work.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The batch work that is run using this method runs in the context and thread apartment of the activity that was created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a>.


A return value of S_OK indicates that the batch work was accepted by the activity to run asynchronously. However, it does not necessarily mean that the batch work successfully completed.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a>
