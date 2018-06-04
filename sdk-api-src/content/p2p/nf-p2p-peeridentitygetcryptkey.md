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

# PeerIdentityGetCryptKey function


## -description



      The <b>PeerIdentityGetCryptKey</b> function retrieves a handle to a cryptographic service provider (CSP).


## -parameters




### -param pwzIdentity [in]

Specifies the peer identity to retrieve the key pair for.


### -param phCryptProv [out]

Receives a pointer to the handle of the  cryptographic service provider (CSP) that contains an AT_KEYEXCHANGE RSA key pair.


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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been manually reset. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An identity that matches the specified name cannot be found.

</td>
</tr>
</table>
 




## -remarks



The  key can be retrieved by calling <a href="https://msdn.microsoft.com/fbd7043d-b2b5-4183-8528-01d3892053e8">CryptGetUserKey</a>.


        When the handle is not required anymore, the application is responsible for releasing the handle by using <a href="https://msdn.microsoft.com/fbd7043d-b2b5-4183-8528-01d3892053e8">CryptReleaseContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/fbd7043d-b2b5-4183-8528-01d3892053e8">CryptGetUserKey</a>



CryptReleaseContext
 

 

