---
UID: NF:comsvcs.ObjectContext.CreateInstance
title: ObjectContext::CreateInstance (comsvcs.h)
description: Creates an object using current object's context. (ObjectContext.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","ObjectContext interface","ObjectContext interface [COM+]","CreateInstance method","ObjectContext.CreateInstance","ObjectContext::CreateInstance","_cos_ObjectContext_CreateInstance","comsvcs/ObjectContext::CreateInstance","cos.objectcontext_createinstance"]
old-location: cos\objectcontext_createinstance.htm
tech.root: cos
ms.assetid: 9719f672-d706-44e3-b976-28d0d0feacd1
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],ObjectContext interface, ObjectContext interface [COM+],CreateInstance method, ObjectContext.CreateInstance, ObjectContext::CreateInstance, _cos_ObjectContext_CreateInstance, comsvcs/ObjectContext::CreateInstance, cos.objectcontext_createinstance
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
 - ObjectContext::CreateInstance
 - comsvcs/ObjectContext::CreateInstance
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
 - ObjectContext.CreateInstance
---

# ObjectContext::CreateInstance


## -description

Creates an object using current object's context.

The object will have context only if its component is registered with COM+.

## -parameters

### -param bstrProgID [in]

The ProgID of the type of object to be instantiated.

### -param pObject [out]

A reference to the new object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-createinstance">CreateInstance</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

When you create an object by using <b>CreateInstance</b>, the new object's context is derived from the current object's <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> and the declarative properties of the new object's component. The new object always executes within the same activity as the object that created it. If the current object has a transaction, the transaction attribute of the new object's component determines whether the new object executes within the scope of that transaction.

If the component's transaction attribute setting either requires a transaction or supports transactions, the new object inherits its creator's transaction. If the component's transaction attribute requires a new transaction, COM+ initiates a new transaction for the new object. If the component's transaction attribute does not support transactions, the new object does not execute under any transaction.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
