---
UID: NF:identitystore.IIdentityStore.GetAt
title: IIdentityStore::GetAt (identitystore.h)
description: Retrieves an IIdentityProvider interface pointer for the specified identity provider.
helpviewer_keywords: ["GetAt","GetAt method [Security]","GetAt method [Security]","IIdentityStore interface","IIdentityStore interface [Security]","GetAt method","IIdentityStore.GetAt","IIdentityStore::GetAt","identitystore/IIdentityStore::GetAt","security.iidentitystore_getat"]
old-location: security\iidentitystore_getat.htm
tech.root: security
ms.assetid: c62212bf-852b-43fb-9abf-b85f4d15b305
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [Security], GetAt method [Security],IIdentityStore interface, IIdentityStore interface [Security],GetAt method, IIdentityStore.GetAt, IIdentityStore::GetAt, identitystore/IIdentityStore::GetAt, security.iidentitystore_getat
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
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
 - IIdentityStore::GetAt
 - identitystore/IIdentityStore::GetAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identitystore.h
api_name:
 - IIdentityStore.GetAt
---

# IIdentityStore::GetAt


## -description

The <b>GetAt</b> method retrieves an <a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a> interface pointer for the specified identity provider.

## -parameters

### -param dwProvider [in]

The index of the identity provider to retrieve.

### -param pProvGuid [in, out]

On output, this parameter receives a pointer to the GUID of the identity provider that this function retrieves.

### -param ppIdentityProvider [out]

A pointer to the <a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a> interface pointer that this method retrieves.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identitystore/nn-identitystore-iidentitystore">IIdentityStore</a>