---
UID: NF:comsvcs.ISecurityCallContext.get__NewEnum
title: ISecurityCallContext::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the security call context collection.
helpviewer_keywords: ["ISecurityCallContext interface [COM+]","get__NewEnum method","ISecurityCallContext.get__NewEnum","ISecurityCallContext::get__NewEnum","_cos_ISecurityCallContext_get__NewEnum","comsvcs/ISecurityCallContext::get__NewEnum","cos.isecuritycallcontext_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ISecurityCallContext interface"]
old-location: cos\isecuritycallcontext_get__newenum.htm
tech.root: cos
ms.assetid: b449a373-2d14-43c5-98b5-ba8119b61e4c
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext interface [COM+],get__NewEnum method, ISecurityCallContext.get__NewEnum, ISecurityCallContext::get__NewEnum, _cos_ISecurityCallContext_get__NewEnum, comsvcs/ISecurityCallContext::get__NewEnum, cos.isecuritycallcontext_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ISecurityCallContext interface
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
 - ISecurityCallContext::get__NewEnum
 - comsvcs/ISecurityCallContext::get__NewEnum
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
 - ISecurityCallContext.get__NewEnum
---

# ISecurityCallContext::get__NewEnum


## -description

Retrieves an enumerator for the security call context collection.

## -parameters

### -param ppEnum [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>