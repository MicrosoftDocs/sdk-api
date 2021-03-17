---
UID: NF:identityprovider.IIdentityProvider.GetProviderPropertyStore
title: IIdentityProvider::GetProviderPropertyStore (identityprovider.h)
description: Retrieves a pointer to the IPropertyStore interface associated with the identity provider.
helpviewer_keywords: ["GetProviderPropertyStore","GetProviderPropertyStore method [Security]","GetProviderPropertyStore method [Security]","IIdentityProvider interface","IIdentityProvider interface [Security]","GetProviderPropertyStore method","IIdentityProvider.GetProviderPropertyStore","IIdentityProvider::GetProviderPropertyStore","identityprovider/IIdentityProvider::GetProviderPropertyStore","security.iidentityprovider_getproviderpropertystore"]
old-location: security\iidentityprovider_getproviderpropertystore.htm
tech.root: security
ms.assetid: e0a8f732-5675-49f7-8c2f-6e5f8f1be957
ms.date: 12/05/2018
ms.keywords: GetProviderPropertyStore, GetProviderPropertyStore method [Security], GetProviderPropertyStore method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],GetProviderPropertyStore method, IIdentityProvider.GetProviderPropertyStore, IIdentityProvider::GetProviderPropertyStore, identityprovider/IIdentityProvider::GetProviderPropertyStore, security.iidentityprovider_getproviderpropertystore
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
 - IIdentityProvider::GetProviderPropertyStore
 - identityprovider/IIdentityProvider::GetProviderPropertyStore
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
 - IIdentityProvider.GetProviderPropertyStore
---

# IIdentityProvider::GetProviderPropertyStore


## -description

The <b>GetProviderPropertyStore</b> method retrieves a pointer to the <b>IPropertyStore</b> interface associated with the identity provider.

## -parameters

### -param ppPropertyStore [out]

A pointer to the global <b>IPropertyStore</b> interface associated with this identity provider.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>