---
UID: NN:comsvcs.ITransactionContextEx
title: ITransactionContextEx (comsvcs.h)
description: Provides basic methods for a generic transactional object that begins a transaction. By calling the methods of this interface, you can compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.
helpviewer_keywords: ["ITransactionContextEx","ITransactionContextEx interface [COM+]","ITransactionContextEx interface [COM+]","described","_cos_ITransactionContextEx_Interface","comsvcs/ITransactionContextEx","cos.itransactioncontextex"]
old-location: cos\itransactioncontextex.htm
tech.root: cos
ms.assetid: cdf3a74f-cdef-4721-9c0d-90af724c24ba
ms.date: 12/05/2018
ms.keywords: ITransactionContextEx, ITransactionContextEx interface [COM+], ITransactionContextEx interface [COM+],described, _cos_ITransactionContextEx_Interface, comsvcs/ITransactionContextEx, cos.itransactioncontextex
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
 - ITransactionContextEx
 - comsvcs/ITransactionContextEx
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
 - ITransactionContextEx
---

# ITransactionContextEx interface


## -description

Provides basic methods for a generic transactional object that begins a transaction. By calling the methods of this interface, you can compose the work of multiple COM+ objects in a single transaction and explicitly commit or abort the transaction.


<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontext">ITransactionContext</a> and <b>ITransactionContextEx</b> provide the same functionality, but unlike <b>ITransactionContextEx</b>, <b>ITransactionContext</b> is compatible with Automation.

## -inheritance

The <b>ITransactionContextEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransactionContextEx</b> also has these types of members:

## -remarks

Using the transaction context object to control a transaction limits the reuse of the business logic driving the transaction and should be used sparingly.

You obtain a reference to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontext">ITransactionContext</a> interface by creating a transaction context object with the appropriate call, as in the following example.


``` syntax
hr = CoCreateInstance(
       CLSID_TransactionContextEx, 
       NULL, 
       CLSCTX_INPROC,
       IID_ITransactionContextEx, 
       (void**)&m_pTransactionContext);

```


## -see-also

<a href="/windows/desktop/cossdk/configuring-transactions">Configuring Transactions</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontext">ITransactionContext</a>



<a href="/windows/desktop/cossdk/transactioncontextex">TransactionContextEx</a>
