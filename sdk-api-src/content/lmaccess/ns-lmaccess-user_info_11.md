---
UID: NS:lmaccess._USER_INFO_11
title: USER_INFO_11 (lmaccess.h)
description: The USER_INFO_11 structure contains information about a user account, including the account name, privilege level, the path to the user's home directory, and other user-related network statistics.
helpviewer_keywords: ["*LPUSER_INFO_11","*PUSER_INFO_11","AF_OP_ACCOUNTS","AF_OP_COMM","AF_OP_PRINT","AF_OP_SERVER","LPUSER_INFO_11","LPUSER_INFO_11 structure pointer [Network Management]","PUSER_INFO_11","PUSER_INFO_11 structure pointer [Network Management]","USER_INFO_11","USER_INFO_11 structure [Network Management]","USER_PRIV_ADMIN","USER_PRIV_GUEST","USER_PRIV_USER","_win32_user_info_11_str","lmaccess/LPUSER_INFO_11","lmaccess/PUSER_INFO_11","lmaccess/USER_INFO_11","netmgmt.user_info_11_str"]
old-location: netmgmt\user_info_11_str.htm
tech.root: NetMgmt
ms.assetid: 718e7143-a6df-4912-954c-cc63bb490044
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_11, *PUSER_INFO_11, AF_OP_ACCOUNTS, AF_OP_COMM, AF_OP_PRINT, AF_OP_SERVER, LPUSER_INFO_11, LPUSER_INFO_11 structure pointer [Network Management], PUSER_INFO_11, PUSER_INFO_11 structure pointer [Network Management], USER_INFO_11, USER_INFO_11 structure [Network Management], USER_PRIV_ADMIN, USER_PRIV_GUEST, USER_PRIV_USER, _win32_user_info_11_str, lmaccess/LPUSER_INFO_11, lmaccess/PUSER_INFO_11, lmaccess/USER_INFO_11, netmgmt.user_info_11_str'
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
req.typenames: USER_INFO_11, *PUSER_INFO_11, *LPUSER_INFO_11
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_11
 - lmaccess/_USER_INFO_11
 - PUSER_INFO_11
 - lmaccess/PUSER_INFO_11
 - USER_INFO_11
 - lmaccess/USER_INFO_11
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
 - USER_INFO_11
---

# USER_INFO_11 structure


## -description

The
				<b>USER_INFO_11</b> structure contains information about a user account, including the account name, privilege level, the path to the user's home directory, and other user-related network statistics.

## -struct-fields

### -field usri11_name

Type: <b>LPWSTR</b>

A pointer to a Unicode character that specifies the name of the user account. Calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function ignore this member. For more information, see the following Remarks section.

### -field usri11_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment associated with the user account. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri11_usr_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a user comment. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri11_full_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the full name of the user. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character.

### -field usri11_priv

Type: <b>DWORD</b>

The level of privilege assigned to the <b>usri11_name</b>  member. For calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> function, this member must be USER_PRIV_USER. For calls to 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>, this member must be the value returned from the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function or the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a> function. This member can be one of the following values. For more information about user and group account rights, see 
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

### -field usri11_auth_flags

Type: <b>DWORD</b>

A set of bit flags defining the user's operator privileges. 




Calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function and the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a> function return a value based on the user's local group membership. If the user is a member of Print Operators, AF_OP_PRINT is set. If the user is a member of Server Operators, AF_OP_SERVER is set. If the user is a member of the Account Operators, AF_OP_ACCOUNTS is set. AF_OP_COMM is never set.

The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

The following restrictions apply:

<ul>
<li>When you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> function, this member must be zero.</li>
<li>When you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function, this member must be the value returned from a call to 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> or to 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>.</li>
</ul>
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

### -field usri11_password_age

Type: <b>DWORD</b>

The number of seconds that have elapsed since the <b>usri11_password</b> member was last changed. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field usri11_home_dir

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path of the home directory for the user specified in the <b>usri11_name</b> member. The string can be <b>NULL</b>.

### -field usri11_parms

Type: <b>LPWSTR</b>

A pointer to a Unicode string that is reserved for use by applications. This string can be a <b>NULL</b> string, or it can have any number of characters before the terminating null character. Microsoft products use this member to store user configuration information. Do not modify this information.

### -field usri11_last_logon

Type: <b>DWORD</b>

The date and time when the last logon occurred. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. 




This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The last logon occurred at the time indicated by the largest retrieved value.

### -field usri11_last_logoff

Type: <b>DWORD</b>

This member is currently not used. 




The date and time when the last logoff occurred. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. A value of zero indicates that the last logoff time is unknown. The 
<b>NetUserAdd</b> function and the 
<b>NetUserSetInfo</b> function ignore this member.

This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The last logoff occurred at the time indicated by the largest retrieved value.

### -field usri11_bad_pw_count

Type: <b>DWORD</b>

The number of times the user tried to log on to this account using an incorrect password. A value of – 1 indicates that the value is unknown. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. 




This member is replicated from the primary domain controller (PDC); it is also maintained on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The number of times the user tried to log on using an incorrect password is the largest value retrieved.

### -field usri11_num_logons

Type: <b>DWORD</b>

The number of times the user has logged on successfully to this account. A value of – 1 indicates that the value is unknown. Calls to the 
<b>NetUserAdd</b> and 
<b>NetUserSetInfo</b> functions ignore this member. 




This member is maintained separately on each backup domain controller (BDC) in the domain. To obtain an accurate value, you must query each BDC in the domain. The number of times the user logged on successfully is the sum of the retrieved values.

### -field usri11_logon_server

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the name of the server to which logon requests are sent. Server names should be preceded by two backslashes (\\). To indicate that the logon request can be handled by any logon server, specify an asterisk (\\*) for the server name. A <b>NULL</b> string indicates that requests should be sent to the domain controller. 




For Windows servers, 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a> return \\*. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field usri11_country_code

Type: <b>DWORD</b>

The country/region code for the user's language of choice.

### -field usri11_workstations

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the names of workstations from which the user can log on. As many as eight workstations can be specified; the names must be separated by commas. A <b>NULL</b> string indicates that there is no restriction. To disable logons from all workstations to this account, set the UF_ACCOUNTDISABLE value in the <b>usri11_flags</b> member.

### -field usri11_max_storage

Type: <b>DWORD</b>

The maximum amount of disk space the user can use. Specify USER_MAXSTORAGE_UNLIMITED to use all available disk space.

### -field usri11_units_per_week

Type: <b>DWORD</b>

The number of equal-length time units into which the week is divided. This value is required to compute the length of the bit string in the <b>usri11_logon_hours</b> member. 




This member must be UNITS_PER_WEEK for LAN Manager 2.0. This element is ignored by the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions.

For service applications, the units must be one of the following values: SAM_DAYS_PER_WEEK, SAM_HOURS_PER_WEEK, or SAM_MINUTES_PER_WEEK.

### -field usri11_logon_hours

Type: <b>PBYTE</b>

A pointer to a 21-byte (168 bits) bit string that specifies the times during which the user can log on. Each bit represents a unique hour in the week, in Greenwich Mean Time (GMT). 




The first bit (bit 0, word 0) is Sunday, 0:00 to 0:59; the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59; and so on. Note that bit 0 in word 0 represents Sunday from 0:00 to 0:59 only if you are in the GMT time zone. In all other cases you must adjust the bits according to your time zone offset (for example, GMT minus 8 hours for Pacific Standard Time).

Specify a <b>NULL</b> pointer in this member when calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> function to indicate no time restriction. Specify a <b>NULL</b> pointer when calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function to indicate that no change is to be made to the times during which the user can log on.

### -field usri11_code_page

Type: <b>DWORD</b>

The code page for the user's language of choice.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel">NetUserDel</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>