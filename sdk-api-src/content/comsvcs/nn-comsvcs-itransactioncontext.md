---
UID: NN:comsvcs.ITransactionContext
title: ITransactionContext
author: windows-sdk-content
description: Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.
old-location: cos\itransactioncontext.htm
old-project: cossdk
ms.assetid: 818fe18b-04ed-4f54-aeb7-b19aafc8a51a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITransactionContext, ITransactionContext interface [COM+], ITransactionContext interface [COM+],described, _cos_ITransactionContext_Interface, comsvcs/ITransactionContext, cos.itransactioncontext
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionContext interface


## -description


Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.


<b>ITransactionContext</b> and <a href="https://msdn.microsoft.com/cdf3a74f-cdef-4721-9c0d-90af724c24ba">ITransactionContextEx</a> provide the same functionality, but unlike <b>ITransactionContextEx</b>, <b>ITransactionContext</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionContext</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITransactionContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransactionContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7ea7c31-225c-4eb1-a358-21c4dab1a1da">Abort</a>
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
<a href="https://msdn.microsoft.com/3dc08700-0872-4d60-a968-cffed974c7b2">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.

</td>
</tr>
</table> 


## -remarks



Using the transaction context object to control a transaction limits the reuse of the business logic driving the transaction and should be used sparingly.

You obtain a reference to the <b>ITransactionContext</b> interface by creating a transaction context object with the appropriate call, as in the following example.

<pre class="syntax" xml:space="preserve"><code>hr = CoCreateInstance(
       CLSID_TransactionContext, 
       NULL, 
       CLSCTX_INPROC,
       IID_ITransactionContext, 
       (void**)&amp;m_pTransactionContext);
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/cdf3a74f-cdef-4721-9c0d-90af724c24ba">ITransactionContextEx</a>



<a href="https://msdn.microsoft.com/efaf1468-4973-472f-af91-85957a52b7df">TransactionContext</a>
 

 

