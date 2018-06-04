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

# _CRYPT_CREDENTIALS structure


## -description


The <b>CRYPT_CREDENTIALS</b> structure contains information about credentials that can be passed as optional input to a remote object retrieval function such as <a href="https://msdn.microsoft.com/2e205f97-be9b-4358-ba22-d475b6a250b7">CryptRetrieveObjectByUrl</a> or <a href="https://msdn.microsoft.com/dd639b43-1560-4e9f-a778-9e20484ae012">CryptGetTimeValidObject</a>.


## -struct-fields




### -field cbSize

The size in bytes of this structure.


### -field pszCredentialsOid

A pointer to a null-terminated string that contains the type of credential object represented by the <b>pvCredentials</b> member.


This member can contain the following possible value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREDENTIAL_OID_PASSWORD_CREDENTIALS"></a><a id="credential_oid_password_credentials"></a><dl>
<dt><b>CREDENTIAL_OID_PASSWORD_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
The <b>pvCredentials</b> member contains a <a href="https://msdn.microsoft.com/21461344-1080-4603-bda1-a92dfda68c15">CRYPT_PASSWORD_CREDENTIALS</a> structure that represents a user name and password combination.

</td>
</tr>
</table>
 


### -field pvCredentials

A pointer to a structure as defined by the <b>pszCredentialsOid</b> member.

