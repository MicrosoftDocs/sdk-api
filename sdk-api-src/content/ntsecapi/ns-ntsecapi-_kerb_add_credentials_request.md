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

# _KERB_ADD_CREDENTIALS_REQUEST structure


## -description


Specifies a  message to add, remove, or replace an extra server credential for a logon session. The <b>SeTcbPrivilege</b> is required to alter another logon account's credentials.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package by calling 
the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbAddExtraCredentialsMessage</b>.


### -field UserName

The user name for the credential.


### -field DomainName

The domain name for the credential.


### -field Password

The password for the credential.


### -field LogonId

The logon ID of the credential. The value of this member can be <b>NULL</b>.


### -field Flags

A value that specifies what to do with the credential. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_ADD_CREDENTIAL"></a><a id="kerb_request_add_credential"></a><dl>
<dt><b>KERB_REQUEST_ADD_CREDENTIAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Add the specified credential to the logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_REPLACE_CREDENTIAL"></a><a id="kerb_request_replace_credential"></a><dl>
<dt><b>KERB_REQUEST_REPLACE_CREDENTIAL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Replace the specified credential in the logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_REQUEST_REMOVE_CREDENTIAL"></a><a id="kerb_request_remove_credential"></a><dl>
<dt><b>KERB_REQUEST_REMOVE_CREDENTIAL</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Remove the specified credential from the logon session.

</td>
</tr>
</table>
 


## -remarks



Calling  the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function with this structure affects only the behavior of the <a href="https://msdn.microsoft.com/838eaaa7-6fce-4ed1-bd69-6e76a804c67b">AcceptSecurityContext (Kerberos)</a> function. Using this structure allows multiple physical and virtual servers to share a single identity.




## -see-also




<a href="https://msdn.microsoft.com/9e806fce-9b3e-4bc9-bd75-a692f0ca5680">KERB_ADD_CREDENTIALS_REQUEST_EX</a>
 

 

