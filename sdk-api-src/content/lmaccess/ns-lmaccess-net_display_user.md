---
UID: NS:lmaccess._NET_DISPLAY_USER
title: NET_DISPLAY_USER (lmaccess.h)
description: The NET_DISPLAY_USER structure contains information that an account manager can access to determine information about user accounts.
helpviewer_keywords: ["*PNET_DISPLAY_USER","NET_DISPLAY_USER","NET_DISPLAY_USER structure [Network Management]","PNET_DISPLAY_USER","PNET_DISPLAY_USER structure pointer [Network Management]","UF_ACCOUNTDISABLE","UF_DONT_EXPIRE_PASSWD","UF_DONT_REQUIRE_PREAUTH","UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED","UF_INTERDOMAIN_TRUST_ACCOUNT","UF_LOCKOUT","UF_NORMAL_ACCOUNT","UF_NOT_DELEGATED","UF_PASSWD_CANT_CHANGE","UF_PASSWD_NOTREQD","UF_PASSWORD_EXPIRED","UF_SCRIPT","UF_SERVER_TRUST_ACCOUNT","UF_SMARTCARD_REQUIRED","UF_TEMP_DUPLICATE_ACCOUNT","UF_TRUSTED_FOR_DELEGATION","UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION","UF_USE_DES_KEY_ONLY","UF_WORKSTATION_TRUST_ACCOUNT","_win32_net_display_user_str","lmaccess/NET_DISPLAY_USER","lmaccess/PNET_DISPLAY_USER","netmgmt.net_display_user_str"]
old-location: netmgmt\net_display_user_str.htm
tech.root: NetMgmt
ms.assetid: 308966f7-448c-4748-bbe7-9ac63afae1d9
ms.date: 12/05/2018
ms.keywords: '*PNET_DISPLAY_USER, NET_DISPLAY_USER, NET_DISPLAY_USER structure [Network Management], PNET_DISPLAY_USER, PNET_DISPLAY_USER structure pointer [Network Management], UF_ACCOUNTDISABLE, UF_DONT_EXPIRE_PASSWD, UF_DONT_REQUIRE_PREAUTH, UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED, UF_INTERDOMAIN_TRUST_ACCOUNT, UF_LOCKOUT, UF_NORMAL_ACCOUNT, UF_NOT_DELEGATED, UF_PASSWD_CANT_CHANGE, UF_PASSWD_NOTREQD, UF_PASSWORD_EXPIRED, UF_SCRIPT, UF_SERVER_TRUST_ACCOUNT, UF_SMARTCARD_REQUIRED, UF_TEMP_DUPLICATE_ACCOUNT, UF_TRUSTED_FOR_DELEGATION, UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION, UF_USE_DES_KEY_ONLY, UF_WORKSTATION_TRUST_ACCOUNT, _win32_net_display_user_str, lmaccess/NET_DISPLAY_USER, lmaccess/PNET_DISPLAY_USER, netmgmt.net_display_user_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NET_DISPLAY_USER, *PNET_DISPLAY_USER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_DISPLAY_USER
 - lmaccess/_NET_DISPLAY_USER
 - PNET_DISPLAY_USER
 - lmaccess/PNET_DISPLAY_USER
 - NET_DISPLAY_USER
 - lmaccess/NET_DISPLAY_USER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - NET_DISPLAY_USER
---

# NET_DISPLAY_USER structure


## -description

The
				<b>NET_DISPLAY_USER</b> structure contains information that an account manager can access to determine information about user accounts.

## -struct-fields

### -field usri1_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the user account.

### -field usri1_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment associated with the user. This string can be a null string, or it can have any number of characters before the terminating null character (MAXCOMMENTSZ).

### -field usri1_flags

Type: <b>DWORD</b>

A set of user account flags. This member can be one or more of the following values. 

Note that setting  user account control flags may require certain <a href="/windows/desktop/SecAuthZ/privileges">privileges</a> and <a href="/windows/desktop/AD/control-access-rights">control access rights</a>. For more information, see the Remarks section of the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

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
The account is currently locked out (blocked). For the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function, this value can be cleared to unlock a previously locked account. This value cannot be used to lock a previously unlocked account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_DONT_EXPIRE_PASSWD"></a><a id="uf_dont_expire_passwd"></a><dl>
<dt><b>UF_DONT_EXPIRE_PASSWD</b></dt>
</dl>
</td>
<td width="60%">
The password will never expire on the account.

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
 The account is marked as "sensitive"; other users cannot act as delegates of this user account.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_SMARTCARD_REQUIRED"></a><a id="uf_smartcard_required"></a><dl>
<dt><b>UF_SMARTCARD_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
 The user is required to log on to the user account with a smart card.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_USE_DES_KEY_ONLY"></a><a id="uf_use_des_key_only"></a><dl>
<dt><b>UF_USE_DES_KEY_ONLY</b></dt>
</dl>
</td>
<td width="60%">
 This principal is restricted to use only Data Encryption Standard (DES) encryption types for keys.

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

<b>Windows XP/2000:  </b>This value is not supported.

</td>
</tr>
</table>
 

The following values describe the account type. Only one value can be set. You cannot change the account type using the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

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
This is a computer account for a workstation or a server that is a member of this domain.

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

### -field usri1_full_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the full name of the user. This string can be a null string, or it can have any number of characters before the terminating null character.

### -field usri1_user_id

Type: <b>DWORD</b>

The relative identifier (RID) of the user. The relative identifier is determined by the accounts database when the user is created. It uniquely defines this user account to the account manager within the domain. For more information about relative identifiers, see 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

### -field usri1_next_index

Type: <b>DWORD</b>

The index of the last entry returned by the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a> function. Pass this value as the <i>Index</i> parameter to 
<b>NetQueryDisplayInformation</b> to return the next logical entry. Note that you should not use the value of this member for any purpose except to retrieve more data with additional calls to 
<b>NetQueryDisplayInformation</b>.

## -see-also

<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>