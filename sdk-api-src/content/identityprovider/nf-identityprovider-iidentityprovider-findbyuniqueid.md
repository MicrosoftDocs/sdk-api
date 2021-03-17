---
UID: NF:identityprovider.IIdentityProvider.FindByUniqueID
title: IIdentityProvider::FindByUniqueID (identityprovider.h)
description: Retrieves a pointer to the IPropertyStore interface instance associated with the specified identity.
helpviewer_keywords: ["FindByUniqueID","FindByUniqueID method [Security]","FindByUniqueID method [Security]","IIdentityProvider interface","IIdentityProvider interface [Security]","FindByUniqueID method","IIdentityProvider.FindByUniqueID","IIdentityProvider::FindByUniqueID","identityprovider/IIdentityProvider::FindByUniqueID","security.iidentityprovider_findbyuniqueid"]
old-location: security\iidentityprovider_findbyuniqueid.htm
tech.root: security
ms.assetid: 26a0e247-0387-4455-9510-bd0e6adc0213
ms.date: 12/05/2018
ms.keywords: FindByUniqueID, FindByUniqueID method [Security], FindByUniqueID method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],FindByUniqueID method, IIdentityProvider.FindByUniqueID, IIdentityProvider::FindByUniqueID, identityprovider/IIdentityProvider::FindByUniqueID, security.iidentityprovider_findbyuniqueid
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
 - IIdentityProvider::FindByUniqueID
 - identityprovider/IIdentityProvider::FindByUniqueID
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
 - IIdentityProvider.FindByUniqueID
---

# IIdentityProvider::FindByUniqueID


## -description

The <b>FindByUniqueID</b> method retrieves a pointer to the <b>IPropertyStore</b> interface instance associated with the specified identity.

## -parameters

### -param lpszUniqueID [in]

The unique identity to find.

### -param ppPropertyStore [out]

A pointer to the instance of the <b>IPropertyStore</b> interface associated with the specified identity.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>