---
UID: NF:identityprovider.IAssociatedIdentityProvider.ChangeCredential
title: IAssociatedIdentityProvider::ChangeCredential (identityprovider.h)
description: Changes the credentials associated with the specified identity.
helpviewer_keywords: ["ChangeCredential","ChangeCredential method [Security]","ChangeCredential method [Security]","IAssociatedIdentityProvider interface","IAssociatedIdentityProvider interface [Security]","ChangeCredential method","IAssociatedIdentityProvider.ChangeCredential","IAssociatedIdentityProvider::ChangeCredential","identityprovider/IAssociatedIdentityProvider::ChangeCredential","identitystore/IAssociatedIdentityProvider::ChangeCredential","security.iassociatedidentityprovider_changecredential"]
old-location: security\iassociatedidentityprovider_changecredential.htm
tech.root: security
ms.assetid: 6a4361a8-8054-434e-9852-fcc20b1086cd
ms.date: 12/05/2018
ms.keywords: ChangeCredential, ChangeCredential method [Security], ChangeCredential method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],ChangeCredential method, IAssociatedIdentityProvider.ChangeCredential, IAssociatedIdentityProvider::ChangeCredential, identityprovider/IAssociatedIdentityProvider::ChangeCredential, identitystore/IAssociatedIdentityProvider::ChangeCredential, security.iassociatedidentityprovider_changecredential
f1_keywords:
- identityprovider/IAssociatedIdentityProvider.ChangeCredential
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
req.idl: Identitystore.idl
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
- IdentityProvider.h
- Identitystore.h
api_name:
- IAssociatedIdentityProvider.ChangeCredential
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssociatedIdentityProvider::ChangeCredential


## -description


The <b>ChangeCredential</b> method changes the credentials associated with the specified identity.


## -parameters




### -param hwndParent [in]

A handle to the parent of the window used to collect account credentials.


### -param lpszUniqueID [in]

The identity for which to change the credentials.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



This method should call <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> to collect account credentials.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iassociatedidentityprovider">IAssociatedIdentityProvider</a>
 

 

