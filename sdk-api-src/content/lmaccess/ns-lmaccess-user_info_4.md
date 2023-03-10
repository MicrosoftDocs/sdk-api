---
UID: NS:lmaccess._USER_INFO_4
title: USER_INFO_4 (lmaccess.h)
description: The USER_INFO_4 structure contains information about a user account, including the account name, password data, privilege level, the path to the user's home directory, security identifier (SID), and other user-related network statistics.
helpviewer_keywords: ["*LPUSER_INFO_4","*PUSER_INFO_4","AF_OP_ACCOUNTS","AF_OP_COMM","AF_OP_PRINT","AF_OP_SERVER","LPUSER_INFO_4","LPUSER_INFO_4 structure pointer [Network Management]","PUSER_INFO_4","PUSER_INFO_4 structure pointer [Network Management]","UF_ACCOUNTDISABLE","UF_DONT_EXPIRE_PASSWD","UF_DONT_REQUIRE_PREAUTH","UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED","UF_HOMEDIR_REQUIRED","UF_INTERDOMAIN_TRUST_ACCOUNT","UF_LOCKOUT","UF_NORMAL_ACCOUNT","UF_NOT_DELEGATED","UF_PASSWD_CANT_CHANGE","UF_PASSWD_NOTREQD","UF_PASSWORD_EXPIRED","UF_SCRIPT","UF_SERVER_TRUST_ACCOUNT","UF_SMARTCARD_REQUIRED","UF_TEMP_DUPLICATE_ACCOUNT","UF_TRUSTED_FOR_DELEGATION","UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION","UF_USE_DES_KEY_ONLY","UF_WORKSTATION_TRUST_ACCOUNT","USER_INFO_4","USER_INFO_4 structure [Network Management]","USER_PRIV_ADMIN","USER_PRIV_GUEST","USER_PRIV_USER","_win32_user_info_4_str","lmaccess/LPUSER_INFO_4","lmaccess/PUSER_INFO_4","lmaccess/USER_INFO_4","netmgmt.user_info_4_str"]
old-location: netmgmt\user_info_4_str.htm
tech.root: NetMgmt
ms.assetid: 66b11a5f-1c2d-4564-8845-9e2fa1f40f3e
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_4, *PUSER_INFO_4, AF_OP_ACCOUNTS, AF_OP_COMM, AF_OP_PRINT, AF_OP_SERVER, LPUSER_INFO_4, LPUSER_INFO_4 structure pointer [Network Management], PUSER_INFO_4, PUSER_INFO_4 structure pointer [Network Management], UF_ACCOUNTDISABLE, UF_DONT_EXPIRE_PASSWD, UF_DONT_REQUIRE_PREAUTH, UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED, UF_HOMEDIR_REQUIRED, UF_INTERDOMAIN_TRUST_ACCOUNT, UF_LOCKOUT, UF_NORMAL_ACCOUNT, UF_NOT_DELEGATED, UF_PASSWD_CANT_CHANGE, UF_PASSWD_NOTREQD, UF_PASSWORD_EXPIRED, UF_SCRIPT, UF_SERVER_TRUST_ACCOUNT, UF_SMARTCARD_REQUIRED, UF_TEMP_DUPLICATE_ACCOUNT, UF_TRUSTED_FOR_DELEGATION, UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION, UF_USE_DES_KEY_ONLY, UF_WORKSTATION_TRUST_ACCOUNT, USER_INFO_4, USER_INFO_4 structure [Network Management], USER_PRIV_ADMIN, USER_PRIV_GUEST, USER_PRIV_USER, _win32_user_info_4_str, lmaccess/LPUSER_INFO_4, lmaccess/PUSER_INFO_4, lmaccess/USER_INFO_4, netmgmt.user_info_4_str'
req.header: lmaccess.h
req.include-header: Lm.h
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
req.typenames: USER_INFO_4, *PUSER_INFO_4, *LPUSER_INFO_4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_4
 - lmaccess/_USER_INFO_4
 - PUSER_INFO_4
 - lmaccess/PUSER_INFO_4
 - USER_INFO_4
 - lmaccess/USER_INFO_4
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
 - USER_INFO_4
---

# USER_INFO_4 structure


## -description

The
				<b>USER_INFO_4</b> structure contains information about a user account, including the account name, password data, privilege level, the path to the user's home directory, security identifier (SID), and other user-related network statistics.

## -struct-fields

### -field usri4_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the user account. For the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function, this member is ignored.

### -field usri4_password

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the password for the user identified by the <b>usri4_name</b> member. The length cannot exceed PWLEN bytes. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function returns a <b>NULL</b> pointer to maintain password security. 




By convention, the length of passwords is limited to LM20_PWLEN characters.

### -field usri4_password_age

Type: <b>DWORD</b>

The number of seconds that have elapsed since the <b>usri4_password</b> member was last changed. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field usri4_priv

Type: <b>DWORD</b>

The level of privilege assigned to the <b>usri4_name</b> member. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. This member can be one of the following values. For more information about user and group account rights, see 
<a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>. 



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

### -field usri4_home_dir

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path of the home directory of the user specified by the <b>usri4_name</b> member. The string can be <b>NULL</b>.

### -field usri4_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment to associate with the user account. The string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri4_flags

Type: <b>DWORD</b>

This member can be one or more of the following values. 

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
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function to clear this value and unlock a previously locked account. You cannot use this value to lock a previously unlocked account.

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

<b>Windows 2000:  </b>This value is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION"></a><a id="uf_trusted_to_authenticate_for_delegation"></a><dl>
<dt><b>UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</b></dt>
</dl>
</td>
<td width="60%">
 The account is trusted to authenticate a user outside of the Kerberos security package and delegate that user through constrained delegation. This is a security-sensitive setting; accounts with this option enabled should be tightly controlled. This setting allows a service running under the account to assert a client's identity and authenticate as that user to specifically configured services on the network.

<b>Windows XP/2000:  </b>This value is ignored.

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

### -field usri4_script_path

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path for the user's logon script file. The script file can be a .CMD file, an .EXE file, or a .BAT file. The string can also be <b>NULL</b>.

### -field usri4_auth_flags

Type: <b>DWORD</b>

The user's operator privileges. 




For the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function, the appropriate value is returned based on the local group membership. If the user is a member of Print Operators, AF_OP_PRINT is set. If the user is a member of Server Operators, AF_OP_SERVER is set. If the user is a member of the Account Operators, AF_OP_ACCOUNTS is set. AF_OP_COMM is never set.

The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_OP_PRINT"></a><a id="af_op_print"></a><dl>
<dt><b>AF_OP_PRINT</b></dt>
</dl>
</td>
<td width="60%">
The print operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_COMM"></a><a id="af_op_comm"></a><dl>
<dt><b>AF_OP_COMM</b></dt>
</dl>
</td>
<td width="60%">
The communications operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_SERVER"></a><a id="af_op_server"></a><dl>
<dt><b>AF_OP_SERVER</b></dt>
</dl>
</td>
<td width="60%">
The server operator privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_OP_ACCOUNTS"></a><a id="af_op_accounts"></a><dl>
<dt><b>AF_OP_ACCOUNTS</b></dt>
</dl>
</td>
<td width="60%">
The accounts operator privilege is enabled.

</td>
</tr>
</table>

### -field usri4_full_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the full name of the user. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri4_usr_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a user comment. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri4_parms

Type: <b>LPWSTR</b>

A pointer to a Unicode string that is reserved for use by applications. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character. Microsoft products use this member to store user configuration information. Do not modify this information.

### -field usri4_workstations

Type: <b>LPWSTR</b>

> [!IMPORTANT]
> You should no longer use **usri4_workstations**. Instead, you can control sign-in access to workstations by configuring the User Rights Assignment settings (**Allow log on locally** and **Deny log on locally**, or **Allow log on through Remote Desktop Services** and **Deny log on through Remote Desktop Services**).

A pointer to a Unicode string that contains the names of workstations from which the user can log on. As many as eight workstations can be specified; the names must be separated by commas. If you do not want to restrict the number of workstations, use a <b>NULL</b> string. To disable logons from all workstations to this account, set the UF_ACCOUNTDISABLE value in the <b>usri4_flags</b> member.

### -field usri4_last_logon

Type: <b>DWORD</b>

The date and time when the last logon occurred. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. This member is ignored by the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions. 




This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The last logon occurred at the time indicated by the largest retrieved value.

### -field usri4_last_logoff

Type: <b>DWORD</b>

This member is currently not used. 




The date and time when the last logoff occurred. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. A value of zero indicates that the last logoff time is unknown.

This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The last logoff occurred at the time indicated by the largest retrieved value.

### -field usri4_acct_expires

Type: <b>DWORD</b>

The date and time when the account expires. This value is stored as the number of seconds elapsed since 00:00:00, January 1, 1970, GMT. A value of TIMEQ_FOREVER indicates that the account never expires.

### -field usri4_max_storage

Type: <b>DWORD</b>

The maximum amount of disk space the user can use. Specify USER_MAXSTORAGE_UNLIMITED to use all available disk space.

### -field usri4_units_per_week

Type: <b>DWORD</b>

The number of equal-length time units into which the week is divided. This value is required to compute the length of the bit string in the <b>usri4_logon_hours</b> member. 




This value must be UNITS_PER_WEEK for LAN Manager 2.0. This element is ignored by the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions.

For service applications, the units must be one of the following values: SAM_DAYS_PER_WEEK, SAM_HOURS_PER_WEEK, or SAM_MINUTES_PER_WEEK.

### -field usri4_logon_hours

Type: <b>PBYTE</b>

A pointer to a 21-byte (168 bits) bit string that specifies the times during which the user can log on. Each bit represents a unique hour in the week, in Greenwich Mean Time (GMT). 




The first bit (bit 0, word 0) is Sunday, 0:00 to 0:59; the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59; and so on. Note that bit 0 in word 0 represents Sunday from 0:00 to 0:59 only if you are in the GMT time zone. In all other cases you must adjust the bits according to your time zone offset (for example, GMT minus 8 hours for Pacific Standard Time).

Specify a <b>NULL</b> pointer in this member when calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> function to indicate no time restriction. Specify a <b>NULL</b> pointer when calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function to indicate that no change is to be made to the times during which the user can log on.

### -field usri4_bad_pw_count

Type: <b>DWORD</b>

The number of times the user tried to log on to the account using an incorrect password. A value of – 1 indicates that the value is unknown. Calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. 




This member is replicated from the primary domain controller (PDC); it is also maintained on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The number of times the user tried to log on using an incorrect password is the largest value retrieved.

### -field usri4_num_logons

Type: <b>DWORD</b>

The number of times the user logged on successfully to this account. A value of – 1 indicates that the value is unknown. Calls to the 
<b>NetUserAdd</b> and 
<b>NetUserSetInfo</b> functions ignore this member. 




This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The number of times the user logged on successfully is the sum of the retrieved values.

### -field usri4_logon_server

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the name of the server to which logon requests are sent. Server names should be preceded by two backslashes (\\). To indicate that the logon request can be handled by any logon server, specify an asterisk (\\*) for the server name. A <b>NULL</b> string indicates that requests should be sent to the domain controller.

For Windows servers, 
the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function returns \\*. 

The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field usri4_country_code

Type: <b>DWORD</b>

The country/region code for the user's language of choice.

### -field usri4_code_page

Type: <b>DWORD</b>

The code page for the user's language of choice.

### -field usri4_user_sid

Type: <b>PSID</b>

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the security identifier (SID) that uniquely identifies the user. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field usri4_primary_group_id

Type: <b>DWORD</b>

The relative identifier (RID) of the Primary Global Group for the user. When you call the 
<b>NetUserAdd</b> function, this member must be DOMAIN_GROUP_RID_USERS (defined in WinNT.h). When you call 
<b>NetUserSetInfo</b>, this member must be the RID of a global group in which the user is enrolled. For more information, see 
<a href="/windows/desktop/SecAuthZ/well-known-sids">Well-Known SIDs</a> and 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

### -field usri4_profile

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies a path to the user's profile. This value can be a <b>NULL</b> string, a local absolute path, or a UNC path.

### -field usri4_home_dir_drive

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the drive letter assigned to the user's home directory for logon purposes.

### -field usri4_password_expired

Type: <b>DWORD</b>

The password expiration information. 




The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function return zero if the password has not expired (and nonzero if it has).

When you call 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> or 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>, specify a nonzero value in this member to inform users that they must change their password at the next logon. To turn off this message, call 
<b>NetUserSetInfo</b> and specify zero in this member. Note that you cannot specify zero to negate the expiration of a password that has already expired.

## -remarks

The
				<b>USER_INFO_4</b> structure can be used with the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a>,
			<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>, and
			<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> functions.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

Note that the 
<b>USER_INFO_4</b> structure supersedes the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3">USER_INFO_3</a> structure on Windows XP and later. It is recommended that applications use 
the <b>USER_INFO_4</b> structure instead of the 
<b>USER_INFO_3</b> structure with the above functions on Windows XP and later.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3">USER_INFO_3</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>