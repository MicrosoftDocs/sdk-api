---
UID: NS:lmaccess._USER_INFO_1
title: "_USER_INFO_1"
author: windows-sdk-content
description: The USER_INFO_1 structure contains information about a user account, including account name, password data, privilege level, and the path to the user's home directory.
old-location: netmgmt\user_info_1_str.htm
old-project: NetMgmt
ms.assetid: f17a1aef-45f1-461f-975d-75221d08277c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPUSER_INFO_1, *PUSER_INFO_1, LPUSER_INFO_1, LPUSER_INFO_1 structure pointer [Network Management], PUSER_INFO_1, PUSER_INFO_1 structure pointer [Network Management], UF_ACCOUNTDISABLE, UF_DONT_EXPIRE_PASSWD, UF_DONT_REQUIRE_PREAUTH, UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED, UF_HOMEDIR_REQUIRED, UF_INTERDOMAIN_TRUST_ACCOUNT, UF_LOCKOUT, UF_NORMAL_ACCOUNT, UF_NOT_DELEGATED, UF_PASSWD_CANT_CHANGE, UF_PASSWD_NOTREQD, UF_PASSWORD_EXPIRED, UF_SCRIPT, UF_SERVER_TRUST_ACCOUNT, UF_SMARTCARD_REQUIRED, UF_TEMP_DUPLICATE_ACCOUNT, UF_TRUSTED_FOR_DELEGATION, UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION, UF_USE_DES_KEY_ONLY, UF_WORKSTATION_TRUST_ACCOUNT, USER_INFO_1, USER_INFO_1 structure [Network Management], USER_PRIV_ADMIN, USER_PRIV_GUEST, USER_PRIV_USER, _USER_INFO_1, _win32_user_info_1_str, lmaccess/LPUSER_INFO_1, lmaccess/PUSER_INFO_1, lmaccess/USER_INFO_1, netmgmt.user_info_1_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: USER_INFO_1, *PUSER_INFO_1, *LPUSER_INFO_1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	USER_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_1 structure


## -description


The
				<b>USER_INFO_1</b> structure contains information about a user account, including account name, password data, privilege level, and the path to the user's home directory.


## -struct-fields




### -field usri1_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the user account. For the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function, this member is ignored. For more information, see the following Remarks section.


### -field usri1_password

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the password of the user indicated by the <b>usri1_name</b> member. The length cannot exceed PWLEN bytes. The 
<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a> and 
<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a> functions return a <b>NULL</b> pointer to maintain password security. 




By convention, the length of passwords is limited to LM20_PWLEN characters.


### -field usri1_password_age

Type: <b>DWORD</b>

The number of seconds that have elapsed since the <b>usri1_password</b> member was last changed. The 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> and 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> functions ignore this member.


### -field usri1_priv

Type: <b>DWORD</b>

The level of privilege assigned to the <b>usri1_name</b> member. When you call the 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> function, this member must be USER_PRIV_USER. When you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function, this member must be the value returned by the 
<b>NetUserGetInfo</b> function or the 
<b>NetUserEnum</b> function. This member can be one of the following values. For more information about user and group account rights, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a>. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USER_PRIV_GUEST"></a><a id="user_priv_guest"></a><dl>
<dt><b>USER_PRIV_GUEST</b></dt>
</dl>
</td>
<td width="60%">
Guest

</td>
</tr>
<tr>
<td width="40%"><a id="USER_PRIV_USER"></a><a id="user_priv_user"></a><dl>
<dt><b>USER_PRIV_USER</b></dt>
</dl>
</td>
<td width="60%">
User

</td>
</tr>
<tr>
<td width="40%"><a id="USER_PRIV_ADMIN"></a><a id="user_priv_admin"></a><dl>
<dt><b>USER_PRIV_ADMIN</b></dt>
</dl>
</td>
<td width="60%">
Administrator

</td>
</tr>
</table>
 


### -field usri1_home_dir

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path of the home directory for the user specified in the <b>usri1_name</b> member. The string can be <b>NULL</b>.


### -field usri1_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment to associate with the user account. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.


### -field usri1_flags

Type: <b>DWORD</b>

This member can be one or more of the following values. 

Note that setting  user account control flags may require certain <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> and <a href="https://msdn.microsoft.com/27ad74bd-ad87-422e-a4a2-02c0d51c4dd4">control access rights</a>. For more information, see the Remarks section of the <a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UF_SCRIPT"></a><a id="uf_script"></a><dl>
<dt><b>UF_SCRIPT</b></dt>
</dl>
</td>
<td width="60%">
The logon script executed. This value must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_ACCOUNTDISABLE"></a><a id="uf_accountdisable"></a><dl>
<dt><b>UF_ACCOUNTDISABLE</b></dt>
</dl>
</td>
<td width="60%">
The user's account is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_HOMEDIR_REQUIRED"></a><a id="uf_homedir_required"></a><dl>
<dt><b>UF_HOMEDIR_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The home directory is required. This value is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_PASSWD_NOTREQD"></a><a id="uf_passwd_notreqd"></a><dl>
<dt><b>UF_PASSWD_NOTREQD</b></dt>
</dl>
</td>
<td width="60%">
No password is required.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_PASSWD_CANT_CHANGE"></a><a id="uf_passwd_cant_change"></a><dl>
<dt><b>UF_PASSWD_CANT_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The user cannot change the password.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_LOCKOUT"></a><a id="uf_lockout"></a><dl>
<dt><b>UF_LOCKOUT</b></dt>
</dl>
</td>
<td width="60%">
The account is currently locked out. You can call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function and clear this value to unlock a previously locked account. You cannot use this value to lock a previously unlocked account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_DONT_EXPIRE_PASSWD"></a><a id="uf_dont_expire_passwd"></a><dl>
<dt><b>UF_DONT_EXPIRE_PASSWD</b></dt>
</dl>
</td>
<td width="60%">
 The password should never expire on the account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED"></a><a id="uf_encrypted_text_password_allowed"></a><dl>
<dt><b>UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
 The user's password is stored under reversible encryption in the Active Directory.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_NOT_DELEGATED"></a><a id="uf_not_delegated"></a><dl>
<dt><b>UF_NOT_DELEGATED</b></dt>
</dl>
</td>
<td width="60%">
 Marks the account as "sensitive"; other users cannot act as delegates of this user account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_SMARTCARD_REQUIRED"></a><a id="uf_smartcard_required"></a><dl>
<dt><b>UF_SMARTCARD_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
 Requires the user to log on to the user account with a smart card.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_USE_DES_KEY_ONLY"></a><a id="uf_use_des_key_only"></a><dl>
<dt><b>UF_USE_DES_KEY_ONLY</b></dt>
</dl>
</td>
<td width="60%">
 Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_DONT_REQUIRE_PREAUTH"></a><a id="uf_dont_require_preauth"></a><dl>
<dt><b>UF_DONT_REQUIRE_PREAUTH</b></dt>
</dl>
</td>
<td width="60%">
 This account does not require Kerberos preauthentication for logon.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_TRUSTED_FOR_DELEGATION"></a><a id="uf_trusted_for_delegation"></a><dl>
<dt><b>UF_TRUSTED_FOR_DELEGATION</b></dt>
</dl>
</td>
<td width="60%">
 The account is enabled for delegation. This is a security-sensitive setting; accounts with this option enabled should be tightly controlled. This setting allows a service running under the account to assume a client's identity and authenticate as that user to other remote servers on the network.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_PASSWORD_EXPIRED"></a><a id="uf_password_expired"></a><dl>
<dt><b>UF_PASSWORD_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
 The user's password has expired.

<b>Windows 2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION"></a><a id="uf_trusted_to_authenticate_for_delegation"></a><dl>
<dt><b>UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</b></dt>
</dl>
</td>
<td width="60%">
 The account is trusted to authenticate a user outside of the Kerberos security package and delegate that user through constrained delegation. This is a security-sensitive setting; accounts with this option enabled should be tightly controlled. This setting allows a service running under the account to assert a client's identity and authenticate as that user to specifically configured services on the network.

<b>Windows 2000:  </b>This value is not supported.

</td>
</tr>
</table>
 

The following values describe the account type. Only one value can be set. You cannot change the account type using the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UF_NORMAL_ACCOUNT"></a><a id="uf_normal_account"></a><dl>
<dt><b>UF_NORMAL_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This is a default account type that represents a typical user.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_TEMP_DUPLICATE_ACCOUNT"></a><a id="uf_temp_duplicate_account"></a><dl>
<dt><b>UF_TEMP_DUPLICATE_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This is an account for users whose primary account is in another domain. This account provides user access to this domain, but not to any domain that trusts this domain. The User Manager refers to this account type as a local user account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_WORKSTATION_TRUST_ACCOUNT"></a><a id="uf_workstation_trust_account"></a><dl>
<dt><b>UF_WORKSTATION_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This is a computer account for a computer that is a member of this domain.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_SERVER_TRUST_ACCOUNT"></a><a id="uf_server_trust_account"></a><dl>
<dt><b>UF_SERVER_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This is a computer account for a backup domain controller that is a member of this domain.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_INTERDOMAIN_TRUST_ACCOUNT"></a><a id="uf_interdomain_trust_account"></a><dl>
<dt><b>UF_INTERDOMAIN_TRUST_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This is a permit to trust account for a domain that trusts other domains.

</td>
</tr>
</table>
 


### -field usri1_script_path

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path for the user's logon script file. The script file can be a .CMD file, an .EXE file, or a .BAT file. The string can also be <b>NULL</b>.


## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a>



<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>



<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

