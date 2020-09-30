---
UID: NF:comsvcs.ISecurityCallContext.get_Item
title: ISecurityCallContext::get_Item (comsvcs.h)
description: Retrieves a specified property in the security call context collection.
helpviewer_keywords: ["ISecurityCallContext interface [COM+]","get_Item method","ISecurityCallContext.get_Item","ISecurityCallContext::get_Item","_cos_ISecurityCallContext_get_Item","comsvcs/ISecurityCallContext::get_Item","cos.isecuritycallcontext_get_item","get_Item","get_Item method [COM+]","get_Item method [COM+]","ISecurityCallContext interface"]
old-location: cos\isecuritycallcontext_get_item.htm
tech.root: cos
ms.assetid: e6561b89-8af6-46cc-aeab-2b007d48fe26
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext interface [COM+],get_Item method, ISecurityCallContext.get_Item, ISecurityCallContext::get_Item, _cos_ISecurityCallContext_get_Item, comsvcs/ISecurityCallContext::get_Item, cos.isecuritycallcontext_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ISecurityCallContext interface
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
 - ISecurityCallContext::get_Item
 - comsvcs/ISecurityCallContext::get_Item
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
 - ISecurityCallContext.get_Item
---

# ISecurityCallContext::get_Item


## -description

Retrieves a specified property in the security call context collection.

## -parameters

### -param name [in]

The name of the property item to be retrieved. See Remarks for information about the available items.

### -param pItem [out]

A reference to the retrieved property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The security call context collection represents a security call context, which provides information about the callers in the chain of calls ending with the current call. For each item in the security call context collection, the following table provides a description, the index name used to retrieve it, and the returned data type of the item.

<table>
<tr>
<th>Item</th>
<th>Description</th>
<th>Index name</th>
<th>Returned type</th>
</tr>
<tr>
<td>Direct Caller
</td>
<td>The immediate caller of the object.</td>
<td>"DirectCaller"
</td>
<td>A <a href="/windows/desktop/cossdk/securityidentity">SecurityIdentity</a> object
</td>
</tr>
<tr>
<td>Original Caller
</td>
<td>The caller that originated the chain of calls to the object.</td>
<td>"OriginalCaller"
</td>
<td>A <a href="/windows/desktop/cossdk/securityidentity">SecurityIdentity</a> object
</td>
</tr>
<tr>
<td>Minimum Authentication Level
</td>
<td>The lowest authentication level used in the chain of calls.</td>
<td>"MinAuthenticationLevel"
</td>
<td>A <b>Long</b></td>
</tr>
<tr>
<td>Number of Callers
</td>
<td>The number of callers in the chain of calls to the object.</td>
<td>"NumCallers"
</td>
<td>A <b>Long</b></td>
</tr>
<tr>
<td>Callers
</td>
<td>The callers in the chain of calls that ends with the current call.</td>
<td>"Callers"</td>
<td>A <a href="/windows/desktop/cossdk/securitycallers">SecurityCallers</a> object
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>