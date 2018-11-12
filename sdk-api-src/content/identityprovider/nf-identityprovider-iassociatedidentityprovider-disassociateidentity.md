---
UID: NF:identityprovider.IAssociatedIdentityProvider.DisassociateIdentity
title: IAssociatedIdentityProvider::DisassociateIdentity
author: windows-sdk-content
description: Disassociates the specified identity from a local user account.
old-location: security\iassociatedidentityprovider_disassociateidentity.htm
tech.root: secauthn
ms.assetid: 6e89b558-bb58-4ef9-86f5-447d5cb0a946
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DisassociateIdentity, DisassociateIdentity method [Security], DisassociateIdentity method [Security],IAssociatedIdentityProvider interface, IAssociatedIdentityProvider interface [Security],DisassociateIdentity method, IAssociatedIdentityProvider.DisassociateIdentity, IAssociatedIdentityProvider::DisassociateIdentity, identityprovider/IAssociatedIdentityProvider::DisassociateIdentity, identitystore/IAssociatedIdentityProvider::DisassociateIdentity, security.iassociatedidentityprovider_disassociateidentity
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
 - IAssociatedIdentityProvider.DisassociateIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/007d5daf-f0cf-4bfb-bd87-bb949bf90126">IAssociatedIdentityProvider</a>
 

 

