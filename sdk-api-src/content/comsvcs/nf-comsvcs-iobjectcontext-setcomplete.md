---
UID: NF:comsvcs.IObjectContext.SetComplete
title: IObjectContext::SetComplete (comsvcs.h)
description: Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.
helpviewer_keywords: ["IObjectContext interface [COM+]","SetComplete method","IObjectContext.SetComplete","IObjectContext::SetComplete","SetComplete","SetComplete method [COM+]","SetComplete method [COM+]","IObjectContext interface","_cos_IObjectContext_SetComplete","comsvcs/IObjectContext::SetComplete","cos.iobjectcontext_setcomplete"]
old-location: cos\iobjectcontext_setcomplete.htm
tech.root: cos
ms.assetid: 8ff25b68-fcb3-4e11-9c74-b49b31806796
ms.date: 12/05/2018
ms.keywords: IObjectContext interface [COM+],SetComplete method, IObjectContext.SetComplete, IObjectContext::SetComplete, SetComplete, SetComplete method [COM+], SetComplete method [COM+],IObjectContext interface, _cos_IObjectContext_SetComplete, comsvcs/IObjectContext::SetComplete, cos.iobjectcontext_setcomplete
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
 - IObjectContext::SetComplete
 - comsvcs/IObjectContext::SetComplete
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
 - IObjectContext.SetComplete
---

# IObjectContext::SetComplete


## -description

Declares that the transaction in which the object is executing can be committed and that the object should be deactivated when it returns from the currently executing method call.



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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

The object is deactivated automatically on return from the method in which it called <b>SetComplete</b>. If the object is the root of an automatic transaction, COM+ attempts to commit the transaction. However, if any object that was participating in the transaction has called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a>, or has called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-disablecommit">DisableCommit</a> and has not subsequently called <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-enablecommit">EnableCommit</a> or <b>SetComplete</b>, the transaction is aborted.

If an object does not need to maintain its state after it returns from a method call, it should call <b>SetComplete</b> so that it can be automatically deactivated as soon as it returns and its resources can be reclaimed.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
