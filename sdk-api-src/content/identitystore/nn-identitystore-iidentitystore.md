---
UID: NN:identitystore.IIdentityStore
title: IIdentityStore (identitystore.h)
description: Provides methods to enumerate and manage identities and identity providers.
helpviewer_keywords: ["IIdentityStore","IIdentityStore interface [Security]","IIdentityStore interface [Security]","described","identitystore/IIdentityStore","security.iidentitystore"]
old-location: security\iidentitystore.htm
tech.root: SecAuthN
ms.assetid: f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6
ms.date: 12/05/2018
ms.keywords: IIdentityStore, IIdentityStore interface [Security], IIdentityStore interface [Security],described, identitystore/IIdentityStore, security.iidentitystore
f1_keywords:
- identitystore/IIdentityStore
dev_langs:
- c++
req.header: identitystore.h
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
- Identitystore.h
api_name:
- IIdentityStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityStore interface


## -description


The <b>IIdentityStore</b> interface
provides methods to enumerate and manage identities and identity providers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIdentityStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIdentityStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-addtocache">AddtoCache</a>
</td>
<td align="left" width="63%">
Caches the specified identity in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-converttosid">ConvertToSid</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) associated with the specified identity and identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-enumerateidentities">EnumerateIdentities</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities across identity providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-getat">GetAt</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a> interface pointer for the specified identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of identity providers registered on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identitystore/nf-identitystore-iidentitystore-reset">Reset</a>
</td>
<td align="left" width="63%">
Sets the current index of the identity enumeration to zero.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>
 

 

