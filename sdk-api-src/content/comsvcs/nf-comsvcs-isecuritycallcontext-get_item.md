---
UID: NF:comsvcs.ISecurityCallContext.get_Item
title: ISecurityCallContext::get_Item
author: windows-sdk-content
description: Retrieves a specified property in the security call context collection.
old-location: cos\isecuritycallcontext_get_item.htm
tech.root: cossdk
ms.assetid: e6561b89-8af6-46cc-aeab-2b007d48fe26
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISecurityCallContext interface [COM+],get_Item method, ISecurityCallContext.get_Item, ISecurityCallContext::get_Item, _cos_ISecurityCallContext_get_Item, comsvcs/ISecurityCallContext::get_Item, cos.isecuritycallcontext_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ISecurityCallContext interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallContext.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ISecurityCallContext.get_Item
: 
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
<td>A <a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a> object
</td>
</tr>
<tr>
<td>Original Caller
</td>
<td>The caller that originated the chain of calls to the object.</td>
<td>"OriginalCaller"
</td>
<td>A <a href="https://msdn.microsoft.com/c6b28695-1b08-490a-8d56-eb55d82f3e7a">SecurityIdentity</a> object
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
<td>A <a href="https://msdn.microsoft.com/164fe12d-eeb3-402f-8aa3-e3545904d9c4">SecurityCallers</a> object
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>
 

 

