---
UID: NF:comsvcs.IAsyncErrorNotify.OnError
title: IAsyncErrorNotify::OnError (comsvcs.h)
description: Called by COM+ when an error occurs in your asynchronous batch work.
helpviewer_keywords: ["IAsyncErrorNotify interface [COM+]","OnError method","IAsyncErrorNotify.OnError","IAsyncErrorNotify::OnError","OnError","OnError method [COM+]","OnError method [COM+]","IAsyncErrorNotify interface","_cos_IAsyncErrorNotify_OnError","comsvcs/IAsyncErrorNotify::OnError","cos.iasyncerrornotify_onerror"]
old-location: cos\iasyncerrornotify_onerror.htm
tech.root: cos
ms.assetid: a48d7733-bbcb-4c03-b265-f112e24c07d9
ms.date: 12/05/2018
ms.keywords: IAsyncErrorNotify interface [COM+],OnError method, IAsyncErrorNotify.OnError, IAsyncErrorNotify::OnError, OnError, OnError method [COM+], OnError method [COM+],IAsyncErrorNotify interface, _cos_IAsyncErrorNotify_OnError, comsvcs/IAsyncErrorNotify::OnError, cos.iasyncerrornotify_onerror
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
 - IAsyncErrorNotify::OnError
 - comsvcs/IAsyncErrorNotify::OnError
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
 - IAsyncErrorNotify.OnError
---

# IAsyncErrorNotify::OnError


## -description

Called by COM+ when an error occurs in your asynchronous batch work.

## -parameters

### -param hr [in]

The <b>HRESULT</b> value of the error that occurred while your batch work was running asynchronously.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

This method should be implemented to gracefully handle errors that occur when your batch work is running asynchronously. Because the process terminates (FailFast) on any unrecoverable error, without this method you have no way of knowing when errors occur in your asynchronous batch work. The process also terminates when this method returns an error as its return value.

The batch work itself is implemented in <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicecall-oncall">IServiceCall::OnCall</a>, and it is run asynchronously by calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-asynchronouscall">IServiceActivity::AsynchronousCall</a> using the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a> pointer that was returned from the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iasyncerrornotify">IAsyncErrorNotify</a>