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

# _DAV_CALLBACK_AUTH_BLOB structure


## -description


Stores an authentication <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that was retrieved by the <a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a> callback function.


## -struct-fields




### -field pBuffer

A pointer to a buffer that receives the authentication <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


### -field ulSize

The size, in bytes, of the buffer that the <b>pBuffer</b> member points to.


### -field ulType

The data type of the buffer that the <b>pBuffer</b> member points to.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
PCCERT_CONTEXT

</td>
</tr>
</table>
 


## -remarks



This structure is included as a member in the <a href="https://msdn.microsoft.com/5414d7b5-b506-4d0a-a4b8-89ab7878d674">DAV_CALLBACK_CRED</a> structure.

The <a href="https://msdn.microsoft.com/96bacda5-8f24-4119-b0ae-82ff8aff54b4">DavFreeCredCallback</a> callback function should free only the buffer that the <b>pBuffer</b> member points to, not the entire structure.




## -see-also




<a href="https://msdn.microsoft.com/47420a67-bf3f-40d9-bfc4-ac2cb2776a40">DAV_CALLBACK_AUTH_UNP</a>



<a href="https://msdn.microsoft.com/6ac191ac-e63f-431f-893b-92c69320db58">DavAuthCallback</a>
 

 

