---
UID: NN:identityprovider.IIdentityProvider
title: IIdentityProvider (identityprovider.h)
description: Represents an identity provider.
old-location: security\iidentityprovider.htm
tech.root: SecAuthN
ms.assetid: 0f23e369-1501-4e72-94d1-dadb9dac5be6
ms.date: 12/05/2018
ms.keywords: IIdentityProvider, IIdentityProvider interface [Security], IIdentityProvider interface [Security],described, identityprovider/IIdentityProvider, security.iidentityprovider
ms.topic: interface
f1_keywords:
- identityprovider/IIdentityProvider
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
- Identityprovider.h
api_name:
- IIdentityProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityProvider interface


## -description


The <b>IIdentityProvider</b> interface represents an identity provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIdentityProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIdentityProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a>
</td>
<td align="left" width="63%">
Allows a calling application to specify the list of identity events for which the application is to be  notified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-create">Create</a>
</td>
<td align="left" width="63%">
Creates a new identity associated with the specified user name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified identity from the identity store or the specified properties from the identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-findbyuniqueid">FindByUniqueID</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IPropertyStore</b> interface instance associated with the specified identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-getidentityenum">GetIdentityEnum</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> interface pointer that can be used to enumerate identities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-getproviderpropertystore">GetProviderPropertyStore</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IPropertyStore</b> interface associated with the identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-import">Import</a>
</td>
<td align="left" width="63%">
Imports an identity to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-unadvise">UnAdvise</a>
</td>
<td align="left" width="63%">
Deletes a connection created by calling the <a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a> method.

</td>
</tr>
</table> 

