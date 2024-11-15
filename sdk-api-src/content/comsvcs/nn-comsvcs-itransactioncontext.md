---
UID: NN:comsvcs.ITransactionContext
title: ITransactionContext (comsvcs.h)
description: Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.
helpviewer_keywords: ["ITransactionContext","ITransactionContext interface [COM+]","ITransactionContext interface [COM+]","described","_cos_ITransactionContext_Interface","comsvcs/ITransactionContext","cos.itransactioncontext"]
old-location: cos\itransactioncontext.htm
tech.root: cos
ms.assetid: 818fe18b-04ed-4f54-aeb7-b19aafc8a51a
ms.date: 12/05/2018
ms.keywords: ITransactionContext, ITransactionContext interface [COM+], ITransactionContext interface [COM+],described, _cos_ITransactionContext_Interface, comsvcs/ITransactionContext, cos.itransactioncontext
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
 - ITransactionContext
 - comsvcs/ITransactionContext
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
 - ITransactionContext
---

# ITransactionContext interface


## -description

Enables you to compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.


<b>ITransactionContext</b> and <a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a> provide the same functionality, but unlike <b>ITransactionContextEx</b>, <b>ITransactionContext</b> is compatible with Automation.

## -inheritance

The <b>ITransactionContext</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITransactionContext</b> also has these types of members:

## -remarks

Using the transaction context object to control a transaction limits the reuse of the business logic driving the transaction and should be used sparingly.

You obtain a reference to the <b>ITransactionContext</b> interface by creating a transaction context object with the appropriate call, as in the following example.


``` syntax
hr = CoCreateInstance(
       CLSID_TransactionContext, 
       NULL, 
       CLSCTX_INPROC,
       IID_ITransactionContext, 
       (void**)&m_pTransactionContext);

```


## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontextex">ITransactionContextEx</a>



<a href="/windows/desktop/cossdk/transactioncontext">TransactionContext</a>
