---
UID: NF:comsvcs.ITransactionContext.CreateInstance
title: ITransactionContext::CreateInstance (comsvcs.h)
description: Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object. (ITransactionContext.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","ITransactionContext interface","ITransactionContext interface [COM+]","CreateInstance method","ITransactionContext.CreateInstance","ITransactionContext::CreateInstance","_cos_ITransactionContext_CreateInstance","comsvcs/ITransactionContext::CreateInstance","cos.itransactioncontext_createinstance"]
old-location: cos\itransactioncontext_createinstance.htm
tech.root: cos
ms.assetid: 3dc08700-0872-4d60-a968-cffed974c7b2
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ITransactionContext interface, ITransactionContext interface [COM+],CreateInstance method, ITransactionContext.CreateInstance, ITransactionContext::CreateInstance, _cos_ITransactionContext_CreateInstance, comsvcs/ITransactionContext::CreateInstance, cos.itransactioncontext_createinstance
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
 - ITransactionContext::CreateInstance
 - comsvcs/ITransactionContext::CreateInstance
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
 - ITransactionContext.CreateInstance
---

# ITransactionContext::CreateInstance


## -description

Creates a COM object that can execute within the scope of the transaction that was initiated by the transaction context object.

## -parameters

### -param pszProgId [in]

A reference to the ProgID of the type of object to be instantiated.

### -param pObject [out]

A reference to the new object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

If the Microsoft Distributed Transaction Coordinator is not running and the object is transactional, the object is successfully created. However, method calls to that object will fail with CONTEXT_E_TMNOTAVAILABLE. Objects cannot recover from this condition and should be released.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactioncontext">ITransactionContext</a>
