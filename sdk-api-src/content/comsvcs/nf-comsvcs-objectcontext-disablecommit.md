---
UID: NF:comsvcs.ObjectContext.DisableCommit
title: ObjectContext::DisableCommit (comsvcs.h)
description: Declares that the object's transactional updates are inconsistent and cannot be committed in their present state.
helpviewer_keywords: ["DisableCommit","DisableCommit method [COM+]","DisableCommit method [COM+]","ObjectContext interface","ObjectContext interface [COM+]","DisableCommit method","ObjectContext.DisableCommit","ObjectContext::DisableCommit","_cos_ObjectContext_DisableCommit","comsvcs/ObjectContext::DisableCommit","cos.objectcontext_disablecommit"]
old-location: cos\objectcontext_disablecommit.htm
tech.root: cos
ms.assetid: cf0e59d9-2760-445e-aa7d-8c2b78457181
ms.date: 12/05/2018
ms.keywords: DisableCommit, DisableCommit method [COM+], DisableCommit method [COM+],ObjectContext interface, ObjectContext interface [COM+],DisableCommit method, ObjectContext.DisableCommit, ObjectContext::DisableCommit, _cos_ObjectContext_DisableCommit, comsvcs/ObjectContext::DisableCommit, cos.objectcontext_disablecommit
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
 - ObjectContext::DisableCommit
 - comsvcs/ObjectContext::DisableCommit
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
 - ObjectContext.DisableCommit
---

# ObjectContext::DisableCommit


## -description

Declares that the object's transactional updates are inconsistent and cannot be committed in their present state.



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
The method completed successfully. The object's transactional updates cannot be committed until the object calls either <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-enablecommit">EnableCommit</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-setcomplete">SetComplete</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-disablecommit">DisableCommit</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The current object doesn't have a context associated with it. This is probably because it was not created with one of the COM+ <b>CreateInstance</b> methods.

</td>
</tr>
</table>

## -remarks

You can use the <b>DisableCommit</b> method to prevent a transaction from committing prematurely between method calls in a stateful object. When an object invokes <b>DisableCommit</b>, it indicates that its work is inconsistent and that it cannot complete its work until it receives further method invocations from the client. It also indicates that it needs to maintain its state to perform that work. This prevents COM+ from deactivating the object and reclaiming its resources on return from a method call. When an object has called <b>DisableCommit</b>, if a client attempts to commit the transaction before the object has called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-enablecommit">EnableCommit</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-setcomplete">SetComplete</a>, the transaction aborts.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
