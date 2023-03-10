---
UID: NF:comsvcs.ITransactionContextEx.Commit
title: ITransactionContextEx::Commit (comsvcs.h)
description: Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method. (ITransactionContextEx.Commit)
helpviewer_keywords: ["Commit","Commit method [COM+]","Commit method [COM+]","ITransactionContextEx interface","ITransactionContextEx interface [COM+]","Commit method","ITransactionContextEx.Commit","ITransactionContextEx::Commit","_cos_ITransactionContextEx_Commit","comsvcs/ITransactionContextEx::Commit","cos.itransactioncontextex_commit"]
old-location: cos\itransactioncontextex_commit.htm
tech.root: cos
ms.assetid: 0ec2e6aa-c534-4c13-9f8b-371f49b96479
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [COM+], Commit method [COM+],ITransactionContextEx interface, ITransactionContextEx interface [COM+],Commit method, ITransactionContextEx.Commit, ITransactionContextEx::Commit, _cos_ITransactionContextEx_Commit, comsvcs/ITransactionContextEx::Commit, cos.itransactioncontextex_commit
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
 - ITransactionContextEx::Commit
 - comsvcs/ITransactionContextEx::Commit
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
 - ITransactionContextEx.Commit
---

# ITransactionContextEx::Commit


## -description

Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method.



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
The transaction was committed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/cossdk/transactioncontextex">TransactionContextEx</a> object is not running under a COM+ process, possibly indicating a corrupted registry entry for the <b>TransactionContextEx</b> component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The transaction was aborted.

</td>
</tr>
</table>

## -remarks

Calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-commit">Commit</a> attempts to commit a transaction. However, the transaction aborts under the following conditions:

<ul>
<li>If a participating object returns from a method after calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>.</li>
<li>If an object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a> and returns without calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a>. 
</li>
<li>If an error causes the Microsoft Distributed Transaction Coordinator (DTC) to abort.
</li>
</ul>
When the method returns, whether the transaction commits or aborts, the transaction ends.


#### Examples

See the example in <a href="/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontextex-abort">ITransactionContextEx::Abort</a>.


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a>
