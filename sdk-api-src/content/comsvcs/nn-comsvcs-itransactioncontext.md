---
UID: NN:comsvcs.ITransactionContext
title: ITransactionContext (comsvcs.h)
author: windows-sdk-content
description: Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.
old-location: cos\itransactioncontext.htm
tech.root: cossdk
ms.assetid: 818fe18b-04ed-4f54-aeb7-b19aafc8a51a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransactionContext, ITransactionContext interface [COM+], ITransactionContext interface [COM+],described, _cos_ITransactionContext_Interface, comsvcs/ITransactionContext, cos.itransactioncontext
ms.topic: interface
f1_keywords: 
 - "comsvcs/ITransactionContext"
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
 - ITransactionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransactionContext interface


## -description


Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.


<b>ITransactionContext</b> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a> provide the same functionality, but unlike <b>ITransactionContextEx</b>, <b>ITransactionContext</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransactionContext</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITransactionContext</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-abort">Abort</a>
</td>
<td align="left" width="63%">
Aborts the work of all COM objects participating in the current transaction. The transaction ends on return from this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-commit">Commit</a>
</td>
<td align="left" width="63%">
Attempts to commit the work of all COM objects participating in the current transaction. The transaction ends on return from this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-createinstance">CreateInstance</a>
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




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/transactioncontext">TransactionContext</a>
 

 

