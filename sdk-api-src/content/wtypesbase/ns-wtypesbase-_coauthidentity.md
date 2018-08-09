---
UID: NS:wtypesbase._COAUTHIDENTITY
title: "_COAUTHIDENTITY"
author: windows-sdk-content
description: Contains a user name and password.
old-location: com\coauthidentity.htm
old-project: com
ms.assetid: ce14f8a6-0495-491a-a5c7-de7c1d3efd95
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: COAUTHIDENTITY, COAUTHIDENTITY structure [COM], SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_UNICODE, _COAUTHIDENTITY, _com_COAUTHIDENTITY, com.coauthidentity, wtypesbase/COAUTHIDENTITY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtypesbase.h
req.include-header: WTypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: COAUTHIDENTITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - COAUTHIDENTITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

