---
UID: NF:comsvcs.IServiceActivity.AsynchronousCall
title: IServiceActivity::AsynchronousCall (comsvcs.h)
description: Performs the user-defined work asynchronously. (IServiceActivity.AsynchronousCall)
helpviewer_keywords: ["AsynchronousCall","AsynchronousCall method [COM+]","AsynchronousCall method [COM+]","IServiceActivity interface","IServiceActivity interface [COM+]","AsynchronousCall method","IServiceActivity.AsynchronousCall","IServiceActivity::AsynchronousCall","_cos_IServiceActivity_AsynchronousCall","comsvcs/IServiceActivity::AsynchronousCall","cos.iserviceactivity_asynchronouscall"]
old-location: cos\iserviceactivity_asynchronouscall.htm
tech.root: cos
ms.assetid: 1d81f2e6-9426-4733-bd1d-0b6ca087cc0a
ms.date: 12/05/2018
ms.keywords: AsynchronousCall, AsynchronousCall method [COM+], AsynchronousCall method [COM+],IServiceActivity interface, IServiceActivity interface [COM+],AsynchronousCall method, IServiceActivity.AsynchronousCall, IServiceActivity::AsynchronousCall, _cos_IServiceActivity_AsynchronousCall, comsvcs/IServiceActivity::AsynchronousCall, cos.iserviceactivity_asynchronouscall
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
 - IServiceActivity::AsynchronousCall
 - comsvcs/IServiceActivity::AsynchronousCall
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
 - IServiceActivity.AsynchronousCall
---

# IServiceActivity::AsynchronousCall


## -description

Performs the user-defined work asynchronously.

## -parameters

### -param pIServiceCall [in]

A pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a> interface that is used to implement the batch work.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The batch work was accepted by the activity to run asynchronously. This return value does not necessarily mean that the batch work successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ASYNC_WORK_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The batch work cannot be added to the asynchronous work queue of the activity.


</td>
</tr>
</table>

## -remarks

The batch work that is run by this method runs in the context and thread apartment of the activity that was created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>
