---
UID: NF:comsvcs.ITransactionContextEx.Commit
title: ITransactionContextEx::Commit
author: windows-sdk-content
description: Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method.
old-location: cos\itransactioncontextex_commit.htm
old-project: cossdk
ms.assetid: 0ec2e6aa-c534-4c13-9f8b-371f49b96479
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Commit, Commit method [COM+], Commit method [COM+],ITransactionContextEx interface, ITransactionContextEx interface [COM+],Commit method, ITransactionContextEx.Commit, ITransactionContextEx::Commit, _cos_ITransactionContextEx_Commit, comsvcs/ITransactionContextEx::Commit, cos.itransactioncontextex_commit
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
 - ITransactionContextEx.Commit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContextEx::Commit


## -description


Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method.


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
The <a href="https://msdn.microsoft.com/5f3f83e0-33fc-4c43-9327-59485c0d8bd3">TransactionContextEx</a> object is not running under a COM+ process, possibly indicating a corrupted registry entry for the <b>TransactionContextEx</b> component.

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



Calling <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> attempts to commit a transaction. However, the transaction aborts under the following conditions:

<ul>
<li>If a participating object returns from a method after calling <a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">SetAbort</a>.</li>
<li>If an object calls <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a> and returns without calling <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> or <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a>. 
</li>
<li>If an error causes the Microsoft Distributed Transaction Coordinator (DTC) to abort.
</li>
</ul>
When the method returns, whether the transaction commits or aborts, the transaction ends.


#### Examples

See the example in <a href="https://msdn.microsoft.com/78f9169f-ecb3-4774-bd28-b1ba83c0838c">ITransactionContextEx::Abort</a>.


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cdf3a74f-cdef-4721-9c0d-90af724c24ba">ITransactionContextEx</a>
 

 

