---
UID: NF:comsvcs.ITransactionProxy.Commit
title: ITransactionProxy::Commit (comsvcs.h)
description: Commits the transaction.
helpviewer_keywords: ["Commit","Commit method [COM+]","Commit method [COM+]","ITransactionProxy interface","ITransactionProxy interface [COM+]","Commit method","ITransactionProxy.Commit","ITransactionProxy::Commit","comsvcs/ITransactionProxy::Commit","cos.itransactionproxy_commit"]
old-location: cos\itransactionproxy_commit.htm
tech.root: cos
ms.assetid: 00b8fe43-22d3-44fd-a1c4-cf3cd36873c6
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [COM+], Commit method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],Commit method, ITransactionProxy.Commit, ITransactionProxy::Commit, comsvcs/ITransactionProxy::Commit, cos.itransactionproxy_commit
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - ITransactionProxy::Commit
 - comsvcs/ITransactionProxy::Commit
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
 - ITransactionProxy.Commit
---

# ITransactionProxy::Commit


## -description

Commits the transaction.

## -parameters

### -param guid [in]

A GUID that identifies the transaction to commit.

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
<dt><b>CONTEXT_E_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The transaction was aborted.


</td>
</tr>
</table>

## -remarks

Calling <b>ITransactionProxy::Commit</b> attempts to commit a transaction. However, the transaction aborts under the following conditions:

<ul>
<li>If a participating object returns from a method after calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>.</li>
<li>If an object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a> and returns without calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a>.</li>
<li>If an error causes the Microsoft Distributed Transaction Coordinator (DTC) to abort.</li>
</ul>
When the method returns, whether the transaction commits or aborts, the transaction ends.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>