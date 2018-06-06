---
UID: NF:comsvcs.ITransactionContextEx.Abort
title: ITransactionContextEx::Abort
author: windows-sdk-content
description: Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.
old-location: cos\itransactioncontextex_abort.htm
old-project: cossdk
ms.assetid: 78f9169f-ecb3-4774-bd28-b1ba83c0838c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: Abort, Abort method [COM+], Abort method [COM+],ITransactionContextEx interface, ITransactionContextEx interface [COM+],Abort method, ITransactionContextEx.Abort, ITransactionContextEx::Abort, _cos_ITransactionContextEx_Abort, comsvcs/ITransactionContextEx::Abort, cos.itransactioncontextex_abort
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
 - ITransactionContextEx.Abort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContextEx::Abort


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
The <a href="https://msdn.microsoft.com/5f3f83e0-33fc-4c43-9327-59485c0d8bd3">TransactionContextEx</a> object is not running under a COM+ process, possibly indicating a corrupted registry entry for the <b>TransactionContextEx</b> component.


</td>
</tr>
</table>
 




## -remarks



Calling <b>Abort</b> ends the transaction on return of the method and automatically deactivates all participating objects. Each resource manager enlisted in the transaction rolls back the operations performed on behalf of those objects.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ITransactionContextEx* pTransactionContext = NULL;
IMyObject* pMyObject = NULL;
boolean bUserCanceled = FALSE;
HRESULT hr;

// Get TransactionContextEx.
hr = CoCreateInstance(CLSID_ITransactionContextEx, 
  NULL, CLSCTX_INPROC, IID_ITransactionContextEx, 
  (void**)&amp;pTransactionContext);
if (FAILED(hr)) throw(hr);

// Create an instance of MyObject.
hr = pTransactionContext-&gt;CreateInstance(CLSID_CMyObject, 
  IID_IMyObject, (void**)&amp;pMyObject);
if (FAILED(hr)) throw(hr);

// Do some work here.

// If something goes wrong, abort the transaction.
if (bUserCanceled) {
    hr = pTransactionContext-&gt;Abort();
    if (FAILED(hr)) throw(hr);

// Otherwise, commit it.
} else {
    hr = pTransactionContext-&gt;Commit();
    if (FAILED(hr)) throw(hr);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cdf3a74f-cdef-4721-9c0d-90af724c24ba">ITransactionContextEx</a>
 

 

