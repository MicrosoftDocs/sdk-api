---
UID: NF:comsvcs.IObjectContext.EnableCommit
title: IObjectContext::EnableCommit (comsvcs.h)
description: Declares that the object's work is not necessarily finished but that its transactional updates are in a consistent state and could be committed in their present form.
helpviewer_keywords: ["EnableCommit","EnableCommit method [COM+]","EnableCommit method [COM+]","IObjectContext interface","IObjectContext interface [COM+]","EnableCommit method","IObjectContext.EnableCommit","IObjectContext::EnableCommit","_cos_IObjectContext_EnableCommit","comsvcs/IObjectContext::EnableCommit","cos.iobjectcontext_enablecommit"]
old-location: cos\iobjectcontext_enablecommit.htm
tech.root: cos
ms.assetid: 6571aadc-bf5a-48c3-817a-66ce444ef96a
ms.date: 12/05/2018
ms.keywords: EnableCommit, EnableCommit method [COM+], EnableCommit method [COM+],IObjectContext interface, IObjectContext interface [COM+],EnableCommit method, IObjectContext.EnableCommit, IObjectContext::EnableCommit, _cos_IObjectContext_EnableCommit, comsvcs/IObjectContext::EnableCommit, cos.iobjectcontext_enablecommit
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
 - IObjectContext::EnableCommit
 - comsvcs/IObjectContext::EnableCommit
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
 - IObjectContext.EnableCommit
---

# IObjectContext::EnableCommit


## -description

Declares that the object's work is not necessarily finished but that its transactional updates are in a consistent state and could be committed in their present form.



## -returns

This method can return the following values.

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
The method completed successfully and the object's transactional updates can now be committed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

When an object calls <b>EnableCommit</b>, it allows the transaction in which it's participating to be committed but it maintains its internal state across calls from its clients until it calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a> or until the transaction completes.

<b>EnableCommit</b> is the default state when an object is activated. Therefore, an object should always call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a> before returning from a method, unless you want the object to maintain its internal state for the next call from a client.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
