---
UID: NF:comsvcs.ObjectContext.get__NewEnum
title: ObjectContext::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the named context object properties.
helpviewer_keywords: ["ObjectContext interface [COM+]","get__NewEnum method","ObjectContext.get__NewEnum","ObjectContext::get__NewEnum","_cos_ObjectContext_get__NewEnum","comsvcs/ObjectContext::get__NewEnum","cos.objectcontext_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ObjectContext interface"]
old-location: cos\objectcontext_get__newenum.htm
tech.root: cos
ms.assetid: 51a0ea69-c602-41db-b3a3-2cf9643c6b3a
ms.date: 12/05/2018
ms.keywords: ObjectContext interface [COM+],get__NewEnum method, ObjectContext.get__NewEnum, ObjectContext::get__NewEnum, _cos_ObjectContext_get__NewEnum, comsvcs/ObjectContext::get__NewEnum, cos.objectcontext_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ObjectContext interface
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
 - ObjectContext::get__NewEnum
 - comsvcs/ObjectContext::get__NewEnum
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
 - ObjectContext.get__NewEnum
---

# ObjectContext::get__NewEnum


## -description

Retrieves an enumerator for the named context object properties.

This property is restricted in Microsoft Visual Basic and cannot be used.

## -parameters

### -param ppEnum [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>