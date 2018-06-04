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

# _COAUTHIDENTITY structure


## -description


Contains a user name and password.


## -struct-fields




### -field User

The user's name.


### -field UserLength

The length of the <b>User</b> string, without the terminating <b>NULL</b>. 


### -field Domain

The domain or workgroup name.


### -field DomainLength

The length of the <b>Domain</b> string, without the terminating <b>NULL</b>. 


### -field Password

The user's password in the domain or workgroup.


### -field PasswordLength

The length of the <b>Password</b> string, without the terminating <b>NULL</b>.


### -field Flags

Indicates whether the strings are Unicode strings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a><a id="sec_winnt_auth_identity_ansi"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ANSI</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The strings are ANSI strings.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a><a id="sec_winnt_auth_identity_unicode"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_UNICODE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The strings are Unicode strings.

</td>
</tr>
</table>
 


## -remarks



COM does not persist the user's password information. For applications that use passwords, please see the documentation on <a href="https://msdn.microsoft.com/library/windows/hardware/mt595945">Cryptography</a> (CryptoAPI). 


This structure is equivalenet to the <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8cbe27b6-c676-49f2-8341-9e180c335636">COAUTHINFO</a>
 

 

