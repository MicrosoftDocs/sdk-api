---
UID: NF:comsvcs.ISecurityIdentityColl.get__NewEnum
title: ISecurityIdentityColl::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the security identity collection.
helpviewer_keywords: ["ISecurityIdentityColl interface [COM+]","get__NewEnum method","ISecurityIdentityColl.get__NewEnum","ISecurityIdentityColl::get__NewEnum","_cos_ISecurityIdentityColl_get__NewEnum","comsvcs/ISecurityIdentityColl::get__NewEnum","cos.isecurityidentitycoll_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ISecurityIdentityColl interface"]
old-location: cos\isecurityidentitycoll_get__newenum.htm
tech.root: cos
ms.assetid: 8e138b0b-cea1-47ca-a73b-473b9f5860db
ms.date: 12/05/2018
ms.keywords: ISecurityIdentityColl interface [COM+],get__NewEnum method, ISecurityIdentityColl.get__NewEnum, ISecurityIdentityColl::get__NewEnum, _cos_ISecurityIdentityColl_get__NewEnum, comsvcs/ISecurityIdentityColl::get__NewEnum, cos.isecurityidentitycoll_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ISecurityIdentityColl interface
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
 - ISecurityIdentityColl::get__NewEnum
 - comsvcs/ISecurityIdentityColl::get__NewEnum
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
 - ISecurityIdentityColl.get__NewEnum
---

# ISecurityIdentityColl::get__NewEnum


## -description

Retrieves an enumerator for the security identity collection.

## -parameters

### -param ppEnum [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>