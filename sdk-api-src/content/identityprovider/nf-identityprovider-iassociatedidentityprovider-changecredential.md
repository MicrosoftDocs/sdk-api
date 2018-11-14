---
UID: NF:identityprovider.IAssociatedIdentityProvider.ChangeCredential
title: IAssociatedIdentityProvider::ChangeCredential
author: windows-sdk-content
description: Changes the credentials associated with the specified identity.
old-location: security\iassociatedidentityprovider_changecredential.htm
tech.root: secauthn
ms.assetid: 6a4361a8-8054-434e-9852-fcc20b1086cd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ChangeCredential, ChangeCredential method [Security], ChangeCredential method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],ChangeCredential method, IAssociatedIdentityProvider.ChangeCredential, IAssociatedIdentityProvider::ChangeCredential, identityprovider/IAssociatedIdentityProvider::ChangeCredential, identitystore/IAssociatedIdentityProvider::ChangeCredential, security.iassociatedidentityprovider_changecredential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- identityprovider.h
: 
- IAssociatedIdentityProvider.ChangeCredential
: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method should call <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> to collect account credentials.




## -see-also




<a href="https://msdn.microsoft.com/007d5daf-f0cf-4bfb-bd87-bb949bf90126">IAssociatedIdentityProvider</a>
 

 

