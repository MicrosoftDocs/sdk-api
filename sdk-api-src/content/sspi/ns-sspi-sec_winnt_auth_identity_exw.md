---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_EXW
tech.root: security
title: SEC_WINNT_AUTH_IDENTITY_EXW
ms.date: 08/03/2022
targetos: Windows
description: The SEC_WINNT_AUTH_IDENTITY_EXW (Unicode) structure contains information about a user.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: 
req.typenames: SEC_WINNT_AUTH_IDENTITY_EXW, *PSEC_WINNT_AUTH_IDENTITY_EXW
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_WINNT_AUTH_IDENTITY_EXW
 - PSEC_WINNT_AUTH_IDENTITY_EXW
 - SEC_WINNT_AUTH_IDENTITY_EXW
f1_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_EXW
 - sspi/_SEC_WINNT_AUTH_IDENTITY_EXW
 - PSEC_WINNT_AUTH_IDENTITY_EXW
 - sspi/PSEC_WINNT_AUTH_IDENTITY_EXW
 - SEC_WINNT_AUTH_IDENTITY_EXW
 - sspi/SEC_WINNT_AUTH_IDENTITY_EXW
dev_langs:
 - c++
---

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

