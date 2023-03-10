---
UID: NF:comsvcs.SecurityProperty.GetOriginalCallerName
title: SecurityProperty::GetOriginalCallerName (comsvcs.h)
description: Retrieves the user name associated with the base process that initiated the sequence of calls from which the call into the current object originated.
helpviewer_keywords: ["GetOriginalCallerName","GetOriginalCallerName method [COM+]","GetOriginalCallerName method [COM+]","SecurityProperty interface","SecurityProperty interface [COM+]","GetOriginalCallerName method","SecurityProperty.GetOriginalCallerName","SecurityProperty::GetOriginalCallerName","_cos_SecurityProperty_GetOriginalCallerName","comsvcs/SecurityProperty::GetOriginalCallerName","cos.securityproperty_getoriginalcallername"]
old-location: cos\securityproperty_getoriginalcallername.htm
tech.root: cos
ms.assetid: ca57950c-3079-42bd-a832-9b7753c61a39
ms.date: 12/05/2018
ms.keywords: GetOriginalCallerName, GetOriginalCallerName method [COM+], GetOriginalCallerName method [COM+],SecurityProperty interface, SecurityProperty interface [COM+],GetOriginalCallerName method, SecurityProperty.GetOriginalCallerName, SecurityProperty::GetOriginalCallerName, _cos_SecurityProperty_GetOriginalCallerName, comsvcs/SecurityProperty::GetOriginalCallerName, cos.securityproperty_getoriginalcallername
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
 - SecurityProperty::GetOriginalCallerName
 - comsvcs/SecurityProperty::GetOriginalCallerName
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
 - SecurityProperty.GetOriginalCallerName
---

# SecurityProperty::GetOriginalCallerName


## -description

Retrieves the user name associated with the base process that initiated the sequence of calls from which the call into the current object originated.

## -parameters

### -param bstrUserName [out]

A reference to the user name associated with the base process that initiated the sequence of calls from which the call into the current object originated.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Generally, an object's original caller is the same process as its original creator. The only situation in which the original caller and the original creator would be different is one in which the original creator passes a reference to another process and the other process initiates the call sequence.

The following scenario illustrates the functionality of this method:

<ol>
<li>Base process 1, running on server A as user A, creates object X, on server B, running as user B.</li>
<li>Then base process 1 passes its reference on object X to base process 2, running on server D as user D.</li>
<li>Base process 2 uses that reference to call into object X.</li>
<li>Object X then calls into object Y, running on server C. If object Y then calls <b>GetOriginalCallerName</b>, the name of user D is returned, not user A, who originally created the object.</li>
</ol>
The path to the original caller is broken if any object along the chain was created by some other means than <a href="/windows/desktop/api/comsvcs/nf-comsvcs-objectcontext-createinstance">ObjectContext::CreateInstance</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-createinstance">ITransactionContext::CreateInstance</a>. For example, if base process 1 uses <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create object X, when object Y calls <b>GetOriginalCallerName</b>, the name it gets back will be the name of user B, not user D. This is because the call sequence is traced back through the objects' context and COM+ can create a context only for an object that is created with either <b>ObjectContext::CreateInstance</b> or <b>ITransactionContext::CreateInstance</b>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-securityproperty">SecurityProperty</a>