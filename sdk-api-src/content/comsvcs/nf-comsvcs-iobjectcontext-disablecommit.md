---
UID: NF:comsvcs.IObjectContext.DisableCommit
title: IObjectContext::DisableCommit
author: windows-sdk-content
description: Declares that the object's transactional updates are in an inconsistent state and cannot be committed in their present state.
old-location: cos\iobjectcontext_disablecommit.htm
tech.root: cossdk
ms.assetid: e83d1223-9b8e-4a92-b98d-9d2b6ed34721
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DisableCommit, DisableCommit method [COM+], DisableCommit method [COM+],IObjectContext interface, IObjectContext interface [COM+],DisableCommit method, IObjectContext.DisableCommit, IObjectContext::DisableCommit, _cos_IObjectContext_DisableCommit, comsvcs/IObjectContext::DisableCommit, cos.iobjectcontext_disablecommit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectContext.DisableCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContext::DisableCommit


## -description


Declares that the object's transactional updates are in an inconsistent state and cannot be committed in their present state.


## -parameters






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
The method completed successfully. The object's transactional updates cannot be committed until the object calls either <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> or <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a> pointer to another object and the other object calls <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The current object does not have a context associated with it. This is probably because it was not created with one of the COM+ CreateInstance methods.

</td>
</tr>
</table>
 




## -remarks



You can use the <b>DisableCommit</b> method to prevent a transaction from committing prematurely between method calls in a stateful object. When an object invokes <b>DisableCommit</b>, it indicates that its work is inconsistent and that it cannot complete its work until it receives further method invocations from the client. It also indicates that it needs to maintain its state to perform that work. This prevents COM+ from deactivating the object and reclaiming its resources on return from a method call. When an object has called <b>DisableCommit</b>, if a client attempts to commit the transaction before the object has called <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> or <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a>, the transaction aborts.

For example, suppose you have a GeneralLedger component that updates a database. A client makes multiple calls to a GeneralLedger object to post entries to various accounts. There's an integrity constraint that says the debits must equal the credits when the final method invocation returns, or the transaction must abort. The GeneralLedger object has an initialization method in which the client informs it of the sequence of calls the client is going to make, and the GeneralLedger object calls <b>DisableCommit</b>. The object maintains its state between calls so that, after the final call in the sequence is made, the object can make sure the integrity constraint is satisfied before allowing its work to be committed.




## -see-also




<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>
 

 

