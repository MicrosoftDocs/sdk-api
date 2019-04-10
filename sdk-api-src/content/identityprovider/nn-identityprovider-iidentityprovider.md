---
UID: NN:identityprovider.IIdentityProvider
title: IIdentityProvider (identityprovider.h)
author: windows-sdk-content
description: Represents an identity provider.
old-location: security\iidentityprovider.htm
tech.root: SecAuthN
ms.assetid: 0f23e369-1501-4e72-94d1-dadb9dac5be6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIdentityProvider, IIdentityProvider interface [Security], IIdentityProvider interface [Security],described, identityprovider/IIdentityProvider, security.iidentityprovider
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
 - Identityprovider.h
api_name:
 - IIdentityProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider interface


## -description


The <b>IIdentityProvider</b> interface represents an identity provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIdentityProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">Advise</a>
</td>
<td align="left" width="63%">
Allows a calling application to specify the list of identity events for which the application is to be  notified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea1a87d-c8c1-43e4-b746-c1bfe98f370b">Create</a>
</td>
<td align="left" width="63%">
Creates a new identity associated with the specified user name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a21aa2eb-2551-4920-a312-34fa327572ca">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified identity from the identity store or the specified properties from the identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26a0e247-0387-4455-9510-bd0e6adc0213">FindByUniqueID</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IPropertyStore</b> interface instance associated with the specified identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e216959-7038-43cf-a57d-bee85d521f58">GetIdentityEnum</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0a8f732-5675-49f7-8c2f-6e5f8f1be957">GetProviderPropertyStore</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IPropertyStore</b> interface associated with the identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16cf4e84-1a68-4794-a456-1a9f5ce4896d">Import</a>
</td>
<td align="left" width="63%">
Imports an identity to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba8a12fc-ea4c-45b5-8339-9cbc88c160db">UnAdvise</a>
</td>
<td align="left" width="63%">
Deletes a connection created by calling the <a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">Advise</a> method.

</td>
</tr>
</table> 

