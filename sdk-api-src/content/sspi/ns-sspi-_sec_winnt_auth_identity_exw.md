---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_EXW
title: "_SEC_WINNT_AUTH_IDENTITY_EXW"
author: windows-sdk-content
description: Contains information about a user. Both an ANSI and Unicode form of this structure are provided.
old-location: security\sec_winnt_auth_identity_ex.htm
old-project: SecAuthN
ms.assetid: 6b95bce8-5613-4403-9bda-16262596bb1b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSEC_WINNT_AUTH_IDENTITY_EXW, PSEC_WINNT_AUTH_IDENTITY_EX, PSEC_WINNT_AUTH_IDENTITY_EX structure pointer [Security], SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_EX, SEC_WINNT_AUTH_IDENTITY_EX structure [Security], SEC_WINNT_AUTH_IDENTITY_EXW, SEC_WINNT_AUTH_IDENTITY_MARSHALLED, SEC_WINNT_AUTH_IDENTITY_ONLY, SEC_WINNT_AUTH_IDENTITY_UNICODE, _SEC_WINNT_AUTH_IDENTITY_EXA, _SEC_WINNT_AUTH_IDENTITY_EXW, _ssp_sec_winnt_auth_identity_ex, security.sec_winnt_auth_identity_ex, sspi/PSEC_WINNT_AUTH_IDENTITY_EX, sspi/SEC_WINNT_AUTH_IDENTITY_EX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_AUTH_IDENTITY_EXW, *PSEC_WINNT_AUTH_IDENTITY_EXW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SEC_WINNT_AUTH_IDENTITY_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SEC_WINNT_AUTH_IDENTITY_EXW structure


## -description


The <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure contains information about a user. Both an ANSI and <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> form of this structure are provided.


## -struct-fields




### -field Version

An unsigned long that indicates the version number of the structure.


### -field Length

An unsigned long that indicates the length, in bytes, of the structure.


### -field User

A Unicode or ANSI string that contains the name of the user account.


### -field UserLength

The length, in characters, of the <b>User</b> string.


### -field Domain

A Unicode or ANSI string that contains the name of the domain for the user account.


### -field DomainLength

The length, in characters, of the <b>Domain</b> string.


### -field Password

A Unicode or ANSI string that contains the user password in plaintext. When you have finished using the password, remove the sensitive information from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -field PasswordLength

The length, in characters, of the <b>Password</b> string.


### -field Flags

An unsigned long flag that indicates the type used by negotiable <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_MARSHALLED"></a><a id="sec_winnt_auth_identity_marshalled"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_MARSHALLED</b></dt>
</dl>
</td>
<td width="60%">
All data is in one buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ONLY"></a><a id="sec_winnt_auth_identity_only"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Used with the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP). Credentials are for identity only. The Kerberos package is directed to not include authorization data in the ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a><a id="sec_winnt_auth_identity_ansi"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ANSI</b></dt>
</dl>
</td>
<td width="60%">
Credentials are in ANSI form.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a><a id="sec_winnt_auth_identity_unicode"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_UNICODE</b></dt>
</dl>
</td>
<td width="60%">
Credentials are in Unicode form.

</td>
</tr>
</table>
 


### -field PackageList

A Unicode or ANSI string that contains a comma-separated list of names of security packages that are available when using the <a href="https://msdn.microsoft.com/3aa7e979-8b55-416d-bed1-28296055d38e">Microsoft Negotiate</a> provider.

Set this to "!ntlm" to specify that the <a href="https://msdn.microsoft.com/35a38858-d36f-45c9-95f4-2541a182f5ac">NTLM</a> package is not to be used.


### -field PackageListLength

The length, in characters, of the <b>PackageList</b> string.


## -remarks



Note that when this structure is used with RPC, the structure must remain valid for the lifetime of the binding handle.



