---
UID: NF:identityprovider.IAssociatedIdentityProvider.DisassociateIdentity
title: IAssociatedIdentityProvider::DisassociateIdentity (identityprovider.h)
author: windows-sdk-content
description: Disassociates the specified identity from a local user account.
old-location: security\iassociatedidentityprovider_disassociateidentity.htm
tech.root: SecAuthN
ms.assetid: 6e89b558-bb58-4ef9-86f5-447d5cb0a946
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisassociateIdentity, DisassociateIdentity method [Security], DisassociateIdentity method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],DisassociateIdentity method, IAssociatedIdentityProvider.DisassociateIdentity, IAssociatedIdentityProvider::DisassociateIdentity, identityprovider/IAssociatedIdentityProvider::DisassociateIdentity, identitystore/IAssociatedIdentityProvider::DisassociateIdentity, security.iassociatedidentityprovider_disassociateidentity
ms.topic: method
f1_keywords: 
 - "identityprovider/IAssociatedIdentityProvider.DisassociateIdentity"
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
 - IAssociatedIdentityProvider.DisassociateIdentity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssociatedIdentityProvider::DisassociateIdentity


## -description


The <b>DisassociateIdentity</b> method disassociates the specified identity from a local user account.


## -parameters




### -param hwndParent [in]

A handle to the parent of the window used to collect account credentials.


### -param lpszUniqueID [in]

The identity to disassociate.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iassociatedidentityprovider">IAssociatedIdentityProvider</a>
 

 

