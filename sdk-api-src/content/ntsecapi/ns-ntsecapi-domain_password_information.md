---
UID: NS:ntsecapi._DOMAIN_PASSWORD_INFORMATION
title: DOMAIN_PASSWORD_INFORMATION (ntsecapi.h)
description: Contains information about a domain's password policy, such as the minimum length for passwords and how unique passwords must be.
helpviewer_keywords: ["*PDOMAIN_PASSWORD_INFORMATION","DOMAIN_LOCKOUT_ADMINS","DOMAIN_PASSWORD_COMPLEX","DOMAIN_PASSWORD_INFORMATION","DOMAIN_PASSWORD_INFORMATION structure [Security]","DOMAIN_PASSWORD_NO_ANON_CHANGE","DOMAIN_PASSWORD_NO_CLEAR_CHANGE","DOMAIN_PASSWORD_STORE_CLEARTEXT","DOMAIN_REFUSE_PASSWORD_CHANGE","PDOMAIN_PASSWORD_INFORMATION","PDOMAIN_PASSWORD_INFORMATION structure pointer [Security]","_lsa_domain_password_information","ntsecapi/DOMAIN_PASSWORD_INFORMATION","ntsecapi/PDOMAIN_PASSWORD_INFORMATION","security.domain_password_information"]
old-location: security\domain_password_information.htm
tech.root: security
ms.assetid: 7dceaf70-d8de-47c0-b940-f0d6a0cca101
ms.date: 12/05/2018
ms.keywords: '*PDOMAIN_PASSWORD_INFORMATION, DOMAIN_LOCKOUT_ADMINS, DOMAIN_PASSWORD_COMPLEX, DOMAIN_PASSWORD_INFORMATION, DOMAIN_PASSWORD_INFORMATION structure [Security], DOMAIN_PASSWORD_NO_ANON_CHANGE, DOMAIN_PASSWORD_NO_CLEAR_CHANGE, DOMAIN_PASSWORD_STORE_CLEARTEXT, DOMAIN_REFUSE_PASSWORD_CHANGE, PDOMAIN_PASSWORD_INFORMATION, PDOMAIN_PASSWORD_INFORMATION structure pointer [Security], _lsa_domain_password_information, ntsecapi/DOMAIN_PASSWORD_INFORMATION, ntsecapi/PDOMAIN_PASSWORD_INFORMATION, security.domain_password_information'
req.header: ntsecapi.h
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
targetos: Windows
req.typenames: DOMAIN_PASSWORD_INFORMATION, *PDOMAIN_PASSWORD_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOMAIN_PASSWORD_INFORMATION
 - ntsecapi/_DOMAIN_PASSWORD_INFORMATION
 - PDOMAIN_PASSWORD_INFORMATION
 - ntsecapi/PDOMAIN_PASSWORD_INFORMATION
 - DOMAIN_PASSWORD_INFORMATION
 - ntsecapi/DOMAIN_PASSWORD_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - DOMAIN_PASSWORD_INFORMATION
---

# DOMAIN_PASSWORD_INFORMATION structure


## -description

The <b>DOMAIN_PASSWORD_INFORMATION</b> structure contains information about a domain's password policy, such as the minimum length for passwords and how unique passwords must be.

It is used in the <a href="/windows/desktop/SecAuthN/msv1-0-changepassword-response">MSV1_0_CHANGEPASSWORD_RESPONSE</a> structure.

## -struct-fields

### -field MinPasswordLength

Specifies the minimum length, in characters, of a valid password.

### -field PasswordHistoryLength

Indicates the number of previous passwords saved in the history list. A user cannot reuse a password in the history list.

### -field PasswordProperties

Flags that describe the password properties. They can be one or more of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_PASSWORD_COMPLEX"></a><a id="domain_password_complex"></a><dl>
<dt><b>DOMAIN_PASSWORD_COMPLEX</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The password must have a mix of at least two of the following types of characters:

<ul>
<li>Uppercase characters</li>
<li>Lowercase characters</li>
<li>Numerals</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_PASSWORD_NO_ANON_CHANGE"></a><a id="domain_password_no_anon_change"></a><dl>
<dt><b>DOMAIN_PASSWORD_NO_ANON_CHANGE</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The password cannot be changed without logging on. Otherwise, if your password has expired, you can change your password and then log on.

</td>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_PASSWORD_NO_CLEAR_CHANGE"></a><a id="domain_password_no_clear_change"></a><dl>
<dt><b>DOMAIN_PASSWORD_NO_CLEAR_CHANGE</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Forces the client to use a protocol that does not allow the domain controller to get the plaintext password.

</td>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_LOCKOUT_ADMINS"></a><a id="domain_lockout_admins"></a><dl>
<dt><b>DOMAIN_LOCKOUT_ADMINS</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Allows the built-in administrator account to be locked out from network logons.

</td>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_PASSWORD_STORE_CLEARTEXT"></a><a id="domain_password_store_cleartext"></a><dl>
<dt><b>DOMAIN_PASSWORD_STORE_CLEARTEXT</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
The directory service is storing a plaintext password for all users instead of a hash function of the password.

</td>
</tr>
<tr>
<td width="40%"><a id="DOMAIN_REFUSE_PASSWORD_CHANGE"></a><a id="domain_refuse_password_change"></a><dl>
<dt><b>DOMAIN_REFUSE_PASSWORD_CHANGE</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Removes the requirement that the machine account password be automatically changed every week.

This value should not be used as it can weaken security.

</td>
</tr>
</table>

### -field MaxPasswordAge

Specifies the maximum length of time that a password can remain the same. Passwords older than this must be changed. Because SAM stores relative times as negative values and absolute times as positive numbers, the time is stored as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure with negative values.

The data type for this member is OLD_LARGE_INTEGER if MIDL_PASS is defined.

### -field MinPasswordAge

Specifies the minimum length of time before a password can be changed. Because SAM stores relative times as negative values and absolute times as positive numbers, the time is stored as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure with negative values.

The data type for this member is OLD_LARGE_INTEGER if MIDL_PASS is defined.