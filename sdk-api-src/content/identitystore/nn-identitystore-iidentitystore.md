---
UID: NN:identitystore.IIdentityStore
title: IIdentityStore
author: windows-driver-content
description: Provides methods to enumerate and manage identities and identity providers.
old-location: security\iidentitystore.htm
old-project: SecAuthN
ms.assetid: f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IIdentityStore, IIdentityStore interface [Security], IIdentityStore interface [Security],described, identitystore/IIdentityStore, security.iidentitystore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Identitystore.h
api_name:
-	IIdentityStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityStore interface


## -description


The <b>IIdentityStore</b> interface
provides methods to enumerate and manage identities and identity providers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIdentityStore</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5ce977bc-41fa-4f80-bb82-76a8bdc40e7e">AddtoCache</a>
</td>
<td align="left" width="63%">
Caches the specified identity in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/484365a9-aeaf-453f-9a5b-6f88b79f8a35">ConvertToSid</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) associated with the specified identity and identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df1a53e0-6296-49ed-b0f0-85e9dc9ab947">EnumerateIdentities</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> interface pointer that can be used to enumerate identities across identity providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a> interface pointer for the specified identity provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of identity providers registered on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Sets the current index of the identity enumeration to zero.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

