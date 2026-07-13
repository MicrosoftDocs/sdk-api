---
UID: NF:comsvcs.IObjectContext.CreateInstance
title: IObjectContext::CreateInstance (comsvcs.h)
description: Creates an object using current object's context. (IObjectContext.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM+]","CreateInstance method [COM+]","IObjectContext interface","IObjectContext interface [COM+]","CreateInstance method","IObjectContext.CreateInstance","IObjectContext::CreateInstance","_cos_IObjectContext_CreateInstance","comsvcs/IObjectContext::CreateInstance","cos.iobjectcontext_createinstance"]
old-location: cos\iobjectcontext_createinstance.htm
tech.root: cos
ms.assetid: 2e870191-5a34-490e-9f3a-cb646fe3f470
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM+], CreateInstance method [COM+],IObjectContext interface, IObjectContext interface [COM+],CreateInstance method, IObjectContext.CreateInstance, IObjectContext::CreateInstance, _cos_IObjectContext_CreateInstance, comsvcs/IObjectContext::CreateInstance, cos.iobjectcontext_createinstance
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
 - IObjectContext::CreateInstance
 - comsvcs/IObjectContext::CreateInstance
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
 - IObjectContext.CreateInstance
---

# IObjectContext::CreateInstance


## -description

Creates an object using current object's context.

## -parameters

### -param rclsid [in]

The CLSID of the type of object to instantiate.

### -param riid [in]

Any interface that's implemented by the object you want to instantiate.

### -param ppv [out]

A reference to the requested interface on the new object. If instantiation fails, this parameter is set to <b>NULL</b>.

## -returns

This method can return the following values.

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
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The component specified by clsid is not registered as a COM component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There's not enough memory available to instantiate the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in the <i>ppvObj</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontext-createinstance">CreateInstance</a> using this pointer. An <b>IObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.


</td>
</tr>
</table>

## -remarks

<b>CreateInstance</b> creates a COM object. However, the object will have context only if its component is registered with COM+.

When you create an object by using <b>CreateInstance</b>, the new object's context is derived from the current object's <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> and the declarative properties of the new object's component. The new object always executes within the same activity as the object that created it. If the current object has a transaction, the transaction attribute of the new object's component determines whether the new object executes within the scope of that transaction.

If the component's transaction attribute setting either requires a transaction or supports transactions, the new object inherits its creator's transaction. If the component's transaction attribute requires a new transaction, COM+ initiates a new transaction for the new object. If the component's transaction attribute does not support transactions, the new object doesn't execute under any transaction.

<b>CreateInstance</b> always returns the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the newly instantiated object. You should immediately cast the returned value to the interface through which you want to communicate with the new object. The interface ID you pass in the <i>riid</i> parameter does not need to be the same interface as the one to which you cast the returned value, but it must be an interface that is implemented by the object you are instantiating.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
