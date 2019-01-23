---
UID: NS:ntsecpkg._SECPKG_PRIMARY_CRED
title: SECPKG_PRIMARY_CRED
author: windows-sdk-content
description: The SECPKG_PRIMARY_CRED structure contains the primary credentials. This structure is used by the LsaApLogonUserEx2 and SpAcceptCredentials functions.
old-location: security\secpkg_primary_cred.htm
tech.root: SecAuthN
ms.assetid: e51fd400-6c3c-4861-ab5c-6c1800b12d31
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSECPKG_PRIMARY_CRED, PRIMARY_CRED_CACHED_LOGON, PRIMARY_CRED_CLEAR_PASSWORD, PRIMARY_CRED_OWF_PASSWORD, PRIMARY_CRED_UPDATE, PSECPKG_PRIMARY_CRED, PSECPKG_PRIMARY_CRED structure pointer [Security], SECPKG_PRIMARY_CRED, SECPKG_PRIMARY_CRED structure [Security], _ssp_secpkg_primary_cred, ntsecpkg/PSECPKG_PRIMARY_CRED, ntsecpkg/SECPKG_PRIMARY_CRED, security.secpkg_primary_cred"
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_PRIMARY_CRED
product: Windows
targetos: Windows
req.typenames: SECPKG_PRIMARY_CRED, *PSECPKG_PRIMARY_CRED
req.redist: 
---

# SECPKG_PRIMARY_CRED structure


## -description


The <b>SECPKG_PRIMARY_CRED</b> structure contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary credentials</a>. This structure is used by the 
<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a> and 
<a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a> functions.


## -struct-fields




### -field LogonId

The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a>.


### -field DownlevelName

A 
<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the Security Accounts Manager account name.


### -field DomainName

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the NetBIOS domain name where the account is located.


### -field Password

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the logon password. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>. For more information on protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -field OldPassword

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the old password. When you have finished using the old password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>.


### -field UserSid

Pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a>.


### -field Flags

The set of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary credentials</a> flags. The following table lists the valid values for the <b>Flags</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_CLEAR_PASSWORD"></a><a id="primary_cred_clear_password"></a><dl>
<dt><b>PRIMARY_CRED_CLEAR_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The passwords are in plaintext.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_OWF_PASSWORD"></a><a id="primary_cred_owf_password"></a><dl>
<dt><b>PRIMARY_CRED_OWF_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The passwords are encrypted using a one-way function.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_UPDATE"></a><a id="primary_cred_update"></a><dl>
<dt><b>PRIMARY_CRED_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
This is a change of existing credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="PRIMARY_CRED_CACHED_LOGON"></a><a id="primary_cred_cached_logon"></a><dl>
<dt><b>PRIMARY_CRED_CACHED_LOGON</b></dt>
</dl>
</td>
<td width="60%">
The credentials were obtained from a cached logon. For more information, see Remarks.

</td>
</tr>
</table>
 


### -field DnsDomainName

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the DNS domain name where the user account is located, if known.


### -field Upn

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the user principal name (UPN), if known.


### -field LogonServer

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that contains the name of the server that processed the logon.


### -field Spare1

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure. Reserved.


### -field Spare2

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure. Reserved.


### -field Spare3

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure. Reserved.


### -field Spare4

A <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure. Reserved.


## -remarks



For cached logons, the RPC identifier of the package that performs the logon is identified by shifting the <b>Flags</b> member to the right by using the PRIMARY_CRED_LOGON_PACKAGE_SHIFT constant defined below.


```cpp
#define PRIMARY_CRED_LOGON_PACKAGE_SHIFT 24

```




