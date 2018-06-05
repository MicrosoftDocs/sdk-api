---
UID: NN:comsvcs.ITransactionContextEx
title: ITransactionContextEx
author: windows-sdk-content
description: Provides basic methods for a generic transactional object that begins a transaction. By calling the methods of this interface, you can compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.
old-location: cos\itransactioncontextex.htm
old-project: cossdk
ms.assetid: cdf3a74f-cdef-4721-9c0d-90af724c24ba
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ITransactionContextEx, ITransactionContextEx interface [COM+], ITransactionContextEx interface [COM+],described, _cos_ITransactionContextEx_Interface, comsvcs/ITransactionContextEx, cos.itransactioncontextex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ITransactionContextEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContextEx interface


## -description


Provides basic methods for a generic transactional object that begins a transaction. By calling the methods of this interface, you can compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.


<a href="https://msdn.microsoft.com/818fe18b-04ed-4f54-aeb7-b19aafc8a51a">ITransactionContext</a> and <b>ITransactionContextEx</b> provide the same functionality, but unlike <b>ITransactionContextEx</b>, <b>ITransactionContext</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionContextEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransactionContextEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransactionContextEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78f9169f-ecb3-4774-bd28-b1ba83c0838c">Abort</a>
</td>
<td align="left" width="63%">
Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49684f80-847b-4613-9148-dd34dc22a476">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.

</td>
</tr>
</table> 


## -remarks



Using the transaction context object to control a transaction limits the reuse of the business logic driving the transaction and should be used sparingly.

You obtain a reference to the <a href="https://msdn.microsoft.com/818fe18b-04ed-4f54-aeb7-b19aafc8a51a">ITransactionContext</a> interface by creating a transaction context object with the appropriate call, as in the following example.

<pre class="syntax" xml:space="preserve"><code>hr = CoCreateInstance(
       CLSID_TransactionContextEx, 
       NULL, 
       CLSCTX_INPROC,
       IID_ITransactionContextEx, 
       (void**)&amp;m_pTransactionContext);
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/ea0e4d7e-2598-4a42-993c-58815f2fa138">Configuring Transactions</a>



<a href="https://msdn.microsoft.com/818fe18b-04ed-4f54-aeb7-b19aafc8a51a">ITransactionContext</a>



<a href="https://msdn.microsoft.com/5f3f83e0-33fc-4c43-9327-59485c0d8bd3">TransactionContextEx</a>
 

 

