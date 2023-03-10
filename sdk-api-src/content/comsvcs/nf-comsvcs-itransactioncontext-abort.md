---
UID: NF:comsvcs.ITransactionContext.Abort
title: ITransactionContext::Abort (comsvcs.h)
description: Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method. (ITransactionContext.Abort)
helpviewer_keywords: ["Abort","Abort method [COM+]","Abort method [COM+]","ITransactionContext interface","ITransactionContext interface [COM+]","Abort method","ITransactionContext.Abort","ITransactionContext::Abort","_cos_ITransactionContext_Abort","comsvcs/ITransactionContext::Abort","cos.itransactioncontext_abort"]
old-location: cos\itransactioncontext_abort.htm
tech.root: cos
ms.assetid: d7ea7c31-225c-4eb1-a358-21c4dab1a1da
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [COM+], Abort method [COM+],ITransactionContext interface, ITransactionContext interface [COM+],Abort method, ITransactionContext.Abort, ITransactionContext::Abort, _cos_ITransactionContext_Abort, comsvcs/ITransactionContext::Abort, cos.itransactioncontext_abort
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
 - ITransactionContext::Abort
 - comsvcs/ITransactionContext::Abort
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
 - ITransactionContext.Abort
---

# ITransactionContext::Abort


## -description

Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The transaction was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/cossdk/transactioncontext">TransactionContext</a> object is not running under a COM+ process, possibly indicating a corrupted registry entry for the <b>TransactionContext</b> component.


</td>
</tr>
</table>

## -remarks

Calling <b>Abort</b> ends the transaction on return of the method and automatically deactivates all participating objects. Each resource manager enlisted in the transaction rolls back the operations performed on behalf of those objects.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontext">ITransactionContext</a>
