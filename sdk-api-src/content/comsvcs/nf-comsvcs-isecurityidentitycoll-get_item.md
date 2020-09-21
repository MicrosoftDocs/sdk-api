---
UID: NF:comsvcs.ISecurityIdentityColl.get_Item
title: ISecurityIdentityColl::get_Item (comsvcs.h)
description: Retrieves a specified property in the security identity collection.
helpviewer_keywords: ["ISecurityIdentityColl interface [COM+]","get_Item method","ISecurityIdentityColl.get_Item","ISecurityIdentityColl::get_Item","_cos_ISecurityIdentityColl_get_Item","comsvcs/ISecurityIdentityColl::get_Item","cos.isecurityidentitycoll_get_item","get_Item","get_Item method [COM+]","get_Item method [COM+]","ISecurityIdentityColl interface"]
old-location: cos\isecurityidentitycoll_get_item.htm
tech.root: cos
ms.assetid: 0cc3a905-ec06-4d8d-8e4a-0774b7e67282
ms.date: 12/05/2018
ms.keywords: ISecurityIdentityColl interface [COM+],get_Item method, ISecurityIdentityColl.get_Item, ISecurityIdentityColl::get_Item, _cos_ISecurityIdentityColl_get_Item, comsvcs/ISecurityIdentityColl::get_Item, cos.isecurityidentitycoll_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ISecurityIdentityColl interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityIdentityColl::get_Item
 - comsvcs/ISecurityIdentityColl::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityIdentityColl.get_Item
---

# ISecurityIdentityColl::get_Item


## -description

Retrieves a specified property in the security identity collection.

## -parameters

### -param name [in]

The name of the property to be retrieved. See Remarks for information about the available properties.

### -param pItem [out]

A reference to the retrieved property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

This collection represents a security identity, which provides information about a particular caller in the chain of calls ending with the current call. For each item in the security identity collection, the following table provides a description, the index name used to retrieve it, and the returned data type of the item.

<table>
<tr>
<th>Item</th>
<th>Description</th>
<th>Index name</th>
<th>Returned type</th>
</tr>
<tr>
<td>SID
</td>
<td>The security identifier of the caller.</td>
<td>"SID"
</td>
<td>V_ARRAY</td>
</tr>
<tr>
<td>Account Name
</td>
<td>The account name that the caller is using.</td>
<td>"AccountName"
</td>
<td>V_BSTR</td>
</tr>
<tr>
<td>Authentication Service
</td>
<td>The authentication service used by the caller, such as NTLMSSP, Kerberos, or SSL.</td>
<td>"AuthenticationService"
</td>
<td>V_I4</td>
</tr>
<tr>
<td>Impersonation Level
</td>
<td>The impersonation level, which indicates how much authority the caller has been given to act on a client's behalf.</td>
<td>"ImpersonationLevel"
</td>
<td>V_I4</td>
</tr>
<tr>
<td>Authentication Level
</td>
<td>The authentication level used by the caller, which indicates the amount of protection given during the call.</td>
<td>"AuthenticationLevel"
</td>
<td>V_I4</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/com--security">COM+ Security</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityidentitycoll">ISecurityIdentityColl</a>