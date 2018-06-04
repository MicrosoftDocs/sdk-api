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

# PeerIdentityDelete function


## -description



      The <b>PeerIdentityDelete</b> function permanently deletes a peer identity. This includes removing all certificates, private keys, and all group information associated with a specified peer identity.


## -parameters




### -param pwzIdentity [in]

Specifies a peer identity to delete.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUPS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The peer identity cannot be deleted because it has  peer groups associated with it.   All peer groups associated with the specified identity must be deleted by using   <a href="https://msdn.microsoft.com/e98df845-71d9-41f9-bf05-b46014e861df">PeerGroupDelete</a> before a call to <a href="https://msdn.microsoft.com/9738f6b1-cd88-4950-bab1-f97613a49e03">PeerIdentityDelete</a> can succeed.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A peer identity that matches the specified name cannot be found.

</td>
</tr>
</table>
 



