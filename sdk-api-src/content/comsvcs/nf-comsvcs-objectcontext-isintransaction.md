---
UID: NF:comsvcs.ObjectContext.IsInTransaction
title: ObjectContext::IsInTransaction (comsvcs.h)
description: Indicates whether the current object is executing in a transaction. (ObjectContext.IsInTransaction)
helpviewer_keywords: ["IsInTransaction","IsInTransaction method [COM+]","IsInTransaction method [COM+]","ObjectContext interface","ObjectContext interface [COM+]","IsInTransaction method","ObjectContext.IsInTransaction","ObjectContext::IsInTransaction","_cos_ObjectContext_IsInTransaction","comsvcs/ObjectContext::IsInTransaction","cos.objectcontext_isintransaction"]
old-location: cos\objectcontext_isintransaction.htm
tech.root: cos
ms.assetid: 843fa973-2c54-4026-8dd9-4ca949b3a894
ms.date: 12/05/2018
ms.keywords: IsInTransaction, IsInTransaction method [COM+], IsInTransaction method [COM+],ObjectContext interface, ObjectContext interface [COM+],IsInTransaction method, ObjectContext.IsInTransaction, ObjectContext::IsInTransaction, _cos_ObjectContext_IsInTransaction, comsvcs/ObjectContext::IsInTransaction, cos.objectcontext_isintransaction
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
 - ObjectContext::IsInTransaction
 - comsvcs/ObjectContext::IsInTransaction
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
 - ObjectContext.IsInTransaction
---

# ObjectContext::IsInTransaction


## -description

Indicates whether the current object is executing in a transaction.

## -parameters

### -param pbIsInTx [out]

<b>TRUE</b> if the current object is executing within a transaction; <b>FALSE</b> otherwise.

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
An unexpected error has occurred. This can happen if one object passes its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a> pointer to another object and the other object calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-isintransaction">IsInTransaction</a> using this pointer. An <b>ObjectContext</b> pointer is not valid outside the context of the object that originally obtained it.

</td>
</tr>
</table>

## -remarks

You can use this method to ensure that an object that requires a transaction never runs without one. For example, if a component that requires a transaction is improperly configured in the Component Services administration tool, you can use this method to determine that the object does not have a transaction. Then you can return an error to alert the user to the problem, or take whatever action is appropriate.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>
