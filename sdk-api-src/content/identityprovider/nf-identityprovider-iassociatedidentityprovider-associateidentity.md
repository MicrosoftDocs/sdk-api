---
UID: NF:identityprovider.IAssociatedIdentityProvider.AssociateIdentity
title: IAssociatedIdentityProvider::AssociateIdentity (identityprovider.h)
description: Associates an identity with a local user account.
helpviewer_keywords: ["AssociateIdentity","AssociateIdentity method [Security]","AssociateIdentity method [Security]","IAssociatedIdentityProvider interface","IAssociatedIdentityProvider interface [Security]","AssociateIdentity method","IAssociatedIdentityProvider.AssociateIdentity","IAssociatedIdentityProvider::AssociateIdentity","identityprovider/IAssociatedIdentityProvider::AssociateIdentity","identitystore/IAssociatedIdentityProvider::AssociateIdentity","security.iassociatedidentityprovider_associateidentity"]
old-location: security\iassociatedidentityprovider_associateidentity.htm
tech.root: security
ms.assetid: 2d1d1da9-c1d0-4970-aad2-928bf6a4aaf0
ms.date: 12/05/2018
ms.keywords: AssociateIdentity, AssociateIdentity method [Security], AssociateIdentity method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],AssociateIdentity method, IAssociatedIdentityProvider.AssociateIdentity, IAssociatedIdentityProvider::AssociateIdentity, identityprovider/IAssociatedIdentityProvider::AssociateIdentity, identitystore/IAssociatedIdentityProvider::AssociateIdentity, security.iassociatedidentityprovider_associateidentity
req.header: identityprovider.h
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
 - IAssociatedIdentityProvider::AssociateIdentity
 - identityprovider/IAssociatedIdentityProvider::AssociateIdentity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IdentityProvider.h
 - Identitystore.h
api_name:
 - IAssociatedIdentityProvider.AssociateIdentity
---

# IAssociatedIdentityProvider::AssociateIdentity


## -description

The <b>AssociateIdentity</b> method associates an identity with a local user account.

## -parameters

### -param hwndParent [in]

A handle to the parent of the window used to collect account credentials.

### -param ppPropertyStore [out]

A pointer to the <b>IPropertyStore</b> interface associated with the identity.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method should call <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> to collect account credentials.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iassociatedidentityprovider">IAssociatedIdentityProvider</a>