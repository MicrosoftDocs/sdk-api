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

# PeerCreatePeerName function


## -description



      The <b>PeerCreatePeerName</b> function  creates a new name based on the existing name of the specified peer identity and classifier. However, a new identity is not created by a call to <b>PeerCreatePeerName</b>.


## -parameters




### -param pwzIdentity [in]

Specifies the identity to use as the basis for the new peer name. If <i>pwzIdentity</i> is <b>NULL</b>, the name created is not based on any peer identity, and is therefore an unsecured name.

This parameter can only be <b>NULL</b> if <i>pwzClassifier</i> is not <b>NULL</b>.


### -param pwzClassifier [in]

Pointer to the Unicode string that contains the new classifier. This classifier is appended to the existing authority portion of the peer name of the specified identity. This string is 150 characters long, including the <b>NULL</b> terminator. Specify <b>NULL</b> to return the peer name of the identity.  

This parameter can only be <b>NULL</b> if <i>pwzIdentity</i> is not <b>NULL</b>.


### -param ppwzPeerName [out]

Pointer that receives a pointer to the new peer name. When this string is not required anymore, free it by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>
 




## -remarks



The parameter  <i>ppwzPeername</i> must be set to null before the <b>PeerCreatePeerName</b> function is called.




## -see-also




<a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>
 

 

