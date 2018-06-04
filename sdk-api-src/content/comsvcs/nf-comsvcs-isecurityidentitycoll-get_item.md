---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/561593c0-d897-4c3a-a4f5-f25351d2c05c">COM+ Security</a>



<a href="https://msdn.microsoft.com/6844bfb2-028f-4155-85a6-b7023432f6cd">ISecurityIdentityColl</a>
 

 

