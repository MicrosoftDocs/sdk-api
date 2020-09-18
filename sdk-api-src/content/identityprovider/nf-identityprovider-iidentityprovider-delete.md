---
UID: NF:identityprovider.IIdentityProvider.Delete
title: IIdentityProvider::Delete (identityprovider.h)
description: Removes the specified identity from the identity store or the specified properties from the identity.
helpviewer_keywords: ["Delete","Delete method [Security]","Delete method [Security]","IIdentityProvider interface","IIdentityProvider interface [Security]","Delete method","IIdentityProvider.Delete","IIdentityProvider::Delete","identityprovider/IIdentityProvider::Delete","security.iidentityprovider_delete"]
old-location: security\iidentityprovider_delete.htm
tech.root: security
ms.assetid: a21aa2eb-2551-4920-a312-34fa327572ca
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Security], Delete method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],Delete method, IIdentityProvider.Delete, IIdentityProvider::Delete, identityprovider/IIdentityProvider::Delete, security.iidentityprovider_delete
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - IIdentityProvider::Delete
 - identityprovider/IIdentityProvider::Delete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.Delete
---

# IIdentityProvider::Delete


## -description

The <b>Delete</b> method removes the specified identity from the identity store or the specified properties from the identity.

## -parameters

### -param lpszUniqueID [in]

The unique name associated with the identity.

### -param pKeywordsToDelete [in, optional]

The names of properties to delete. If the value of this parameter is <b>NULL</b>, the identity is deleted.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>