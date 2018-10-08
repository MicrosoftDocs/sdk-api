---
UID: NF:identityprovider.IAssociatedIdentityProvider.AssociateIdentity
title: IAssociatedIdentityProvider::AssociateIdentity
author: windows-sdk-content
description: Associates an identity with a local user account.
old-location: security\iassociatedidentityprovider_associateidentity.htm
tech.root: secauthn
ms.assetid: 2d1d1da9-c1d0-4970-aad2-928bf6a4aaf0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: AssociateIdentity, AssociateIdentity method [Security], AssociateIdentity method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],AssociateIdentity method, IAssociatedIdentityProvider.AssociateIdentity, IAssociatedIdentityProvider::AssociateIdentity, identityprovider/IAssociatedIdentityProvider::AssociateIdentity, identitystore/IAssociatedIdentityProvider::AssociateIdentity, security.iassociatedidentityprovider_associateidentity
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
 - IAssociatedIdentityProvider.AssociateIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method should call <a href="https://msdn.microsoft.com/946ac279-d30a-4a6c-a76d-d93597121427">CredUIPromptForWindowsCredentials</a> to collect account credentials.




## -see-also




<a href="https://msdn.microsoft.com/007d5daf-f0cf-4bfb-bd87-bb949bf90126">IAssociatedIdentityProvider</a>
 

 

