---
UID: NF:identityprovider.IIdentityProvider.Create
title: IIdentityProvider::Create (identityprovider.h)
description: Creates a new identity associated with the specified user name.
helpviewer_keywords: ["Create","Create method [Security]","Create method [Security]","IIdentityProvider interface","IIdentityProvider interface [Security]","Create method","IIdentityProvider.Create","IIdentityProvider::Create","identityprovider/IIdentityProvider::Create","security.iidentityprovider_create"]
old-location: security\iidentityprovider_create.htm
tech.root: security
ms.assetid: 6ea1a87d-c8c1-43e4-b746-c1bfe98f370b
ms.date: 12/05/2018
ms.keywords: Create, Create method [Security], Create method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],Create method, IIdentityProvider.Create, IIdentityProvider::Create, identityprovider/IIdentityProvider::Create, security.iidentityprovider_create
f1_keywords:
- identityprovider/IIdentityProvider.Create
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Identityprovider.h
api_name:
- IIdentityProvider.Create
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityProvider::Create


## -description


The <b>Create</b> method creates a new identity associated with the specified user name.


## -parameters




### -param lpszUserName [in]

The user name with which to associate the new identity.


### -param ppPropertyStore [out]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface that represents the property store associated with the new identity.


### -param pKeywordsToAdd [in, optional]

The properties to associate with the new identity.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>
 

 

