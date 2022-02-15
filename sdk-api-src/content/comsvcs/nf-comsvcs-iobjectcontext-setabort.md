---
UID: NF:comsvcs.IObjectContext.SetAbort
title: IObjectContext::SetAbort (comsvcs.h)
description: Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated when it returns from the currently executing method call.
helpviewer_keywords: ["IObjectContext interface [COM+]","SetAbort method","IObjectContext.SetAbort","IObjectContext::SetAbort","SetAbort","SetAbort method [COM+]","SetAbort method [COM+]","IObjectContext interface","_cos_IObjectContext_SetAbort","comsvcs/IObjectContext::SetAbort","cos.iobjectcontext_setabort"]
old-location: cos\iobjectcontext_setabort.htm
tech.root: cos
ms.assetid: c254305f-1fc5-417e-b93b-d5e2b36e9e39
ms.date: 12/05/2018
ms.keywords: IObjectContext interface [COM+],SetAbort method, IObjectContext.SetAbort, IObjectContext::SetAbort, SetAbort, SetAbort method [COM+], SetAbort method [COM+],IObjectContext interface, _cos_IObjectContext_SetAbort, comsvcs/IObjectContext::SetAbort, cos.iobjectcontext_setabort
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
 - IObjectContext::SetAbort
 - comsvcs/IObjectContext::SetAbort
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
 - IObjectContext.SetAbort
---

# IObjectContext::SetAbort


## -description

Declares that the transaction in which the object is executing must be aborted and that the object should be deactivated when it returns from the currently executing method call.



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
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setabort">SetAbort</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

The object is deactivated automatically on return from the method in which it called <b>SetAbort</b>. If the object is the root of an automatic transaction, COM+ aborts the transaction. If the object is transactional but not the root of an automatic transaction, the transaction in which it's participating is doomed to abort.

You can call <b>SetAbort</b> in error handlers to ensure that a transaction aborts when an error occurs. You can also call <b>SetAbort</b> at the beginning of a method to prevent your object from committing prematurely in the event of an unexpected return and then, if all goes well, call <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-setcomplete">SetComplete</a> just before the method returns.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
