---
UID: NN:identityprovider.IAssociatedIdentityProvider
title: IAssociatedIdentityProvider
author: windows-sdk-content
description: Allows an identity provider to associate identities with local user accounts.
old-location: security\iassociatedidentityprovider.htm
tech.root: secauthn
ms.assetid: 007d5daf-f0cf-4bfb-bd87-bb949bf90126
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IAssociatedIdentityProvider, IAssociatedIdentityProvider interface [Security], IAssociatedIdentityProvider interface [Security],described, identityprovider/IAssociatedIdentityProvider, identitystore/IAssociatedIdentityProvider, security.iassociatedidentityprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IAssociatedIdentityProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssociatedIdentityProvider interface


## -description


The <b>IAssociatedIdentityProvider</b> interface allows an identity provider to associate identities with local user accounts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssociatedIdentityProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAssociatedIdentityProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssociatedIdentityProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d1d1da9-c1d0-4970-aad2-928bf6a4aaf0">AssociateIdentity</a>
</td>
<td align="left" width="63%">
Associates an identity with a local user account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a4361a8-8054-434e-9852-fcc20b1086cd">ChangeCredential</a>
</td>
<td align="left" width="63%">
Changes the credentials associated with the specified identity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e89b558-bb58-4ef9-86f5-447d5cb0a946">DisassociateIdentity</a>
</td>
<td align="left" width="63%">
Disassociates the specified identity from a local user account.


</td>
</tr>
</table> 

