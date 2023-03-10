---
UID: NF:comsvcs.ISecurityCallersColl.get__NewEnum
title: ISecurityCallersColl::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the security callers collection.
helpviewer_keywords: ["ISecurityCallersColl interface [COM+]","get__NewEnum method","ISecurityCallersColl.get__NewEnum","ISecurityCallersColl::get__NewEnum","_cos_ISecurityCallersColl_get__NewEnum","comsvcs/ISecurityCallersColl::get__NewEnum","cos.isecuritycallerscoll_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ISecurityCallersColl interface"]
old-location: cos\isecuritycallerscoll_get__newenum.htm
tech.root: cos
ms.assetid: 80fb8fe7-0f8f-497c-a046-82f19d6469d8
ms.date: 12/05/2018
ms.keywords: ISecurityCallersColl interface [COM+],get__NewEnum method, ISecurityCallersColl.get__NewEnum, ISecurityCallersColl::get__NewEnum, _cos_ISecurityCallersColl_get__NewEnum, comsvcs/ISecurityCallersColl::get__NewEnum, cos.isecuritycallerscoll_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ISecurityCallersColl interface
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
 - ISecurityCallersColl::get__NewEnum
 - comsvcs/ISecurityCallersColl::get__NewEnum
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
 - ISecurityCallersColl.get__NewEnum
---

# ISecurityCallersColl::get__NewEnum


## -description

Retrieves an enumerator for the security callers collection.

## -parameters

### -param ppEnum [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallerscoll">ISecurityCallersColl</a>