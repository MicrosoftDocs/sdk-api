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

# _DOMAIN_PASSWORD_INFORMATION structure


## -description


The <b>DOMAIN_PASSWORD_INFORMATION</b> structure contains information about a domain's password policy, such as the minimum length for passwords and how unique passwords must be.

It is used in the <a href="https://msdn.microsoft.com/45946272-7350-42f3-af54-9012829bf1de">MSV1_0_CHANGEPASSWORD_RESPONSE</a> structure.


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

Specifies the maximum length of time that a password can remain the same. Passwords older than this must be changed. Because SAM stores relative times as negative values and absolute times as positive numbers, the time is stored as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure with negative values.

The data type for this member is OLD_LARGE_INTEGER if MIDL_PASS is defined.


### -field MinPasswordAge

Specifies the minimum length of time before a password can be changed. Because SAM stores relative times as negative values and absolute times as positive numbers, the time is stored as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure with negative values.

The data type for this member is OLD_LARGE_INTEGER if MIDL_PASS is defined.

