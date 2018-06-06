---
UID: NF:comsvcs.ITransactionContext.Abort
title: ITransactionContext::Abort
author: windows-sdk-content
description: Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.
old-location: cos\itransactioncontext_abort.htm
old-project: cossdk
ms.assetid: d7ea7c31-225c-4eb1-a358-21c4dab1a1da
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: Abort, Abort method [COM+], Abort method [COM+],ITransactionContext interface, ITransactionContext interface [COM+],Abort method, ITransactionContext.Abort, ITransactionContext::Abort, _cos_ITransactionContext_Abort, comsvcs/ITransactionContext::Abort, cos.itransactioncontext_abort
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionContext.Abort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContext::Abort


## -description


Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.


## -parameters






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
The <a href="https://msdn.microsoft.com/efaf1468-4973-472f-af91-85957a52b7df">TransactionContext</a> object is not running under a COM+ process, possibly indicating a corrupted registry entry for the <b>TransactionContext</b> component.


</td>
</tr>
</table>
 




## -remarks



Calling <b>Abort</b> ends the transaction on return of the method and automatically deactivates all participating objects. Each resource manager enlisted in the transaction rolls back the operations performed on behalf of those objects.





## -see-also




<a href="https://msdn.microsoft.com/818fe18b-04ed-4f54-aeb7-b19aafc8a51a">ITransactionContext</a>
 

 

