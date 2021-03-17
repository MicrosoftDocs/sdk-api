---
UID: NF:lmaccess.NetUserSetInfo
title: NetUserSetInfo function (lmaccess.h)
description: The NetUserSetInfo function sets the parameters of a user account.
helpviewer_keywords: ["0","1","1003","1005","1006","1007","1008","1009","1010","1011","1012","1014","1017","1020","1024","1051","1052","1053","2","21","22","3","4","NetUserSetInfo","NetUserSetInfo function [Network Management]","_win32_netusersetinfo","lmaccess/NetUserSetInfo","netmgmt.netusersetinfo"]
old-location: netmgmt\netusersetinfo.htm
tech.root: NetMgmt
ms.assetid: ffe49d4b-e7e8-4982-8087-59bb7534b257
ms.date: 12/05/2018
ms.keywords: 0, 1, 1003, 1005, 1006, 1007, 1008, 1009, 1010, 1011, 1012, 1014, 1017, 1020, 1024, 1051, 1052, 1053, 2, 21, 22, 3, 4, NetUserSetInfo, NetUserSetInfo function [Network Management], _win32_netusersetinfo, lmaccess/NetUserSetInfo, netmgmt.netusersetinfo
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetUserSetInfo
 - lmaccess/NetUserSetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetUserSetInfo
---

# NetUserSetInfo function


## -description

The
				<b>NetUserSetInfo</b> function sets the parameters of a user account.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param username [in]

A pointer to a constant string that specifies the name of the user account for which to set information. For more information, see the following Remarks section.

### -param level [in]

The information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user account name. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_0">USER_INFO_0</a> structure. Use this structure to specify a new group name. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the user account. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies level one information and additional attributes about the user account. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_2">USER_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3">USER_INFO_3</a> structure. Note that  it is recommended that you use 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_4">USER_INFO_4</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
 Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_4">USER_INFO_4</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="21"></a><dl>
<dt><b>21</b></dt>
</dl>
</td>
<td width="60%">
Specifies a one-way encrypted LAN Manager 2.<i>x</i>-compatible password. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_21">USER_INFO_21</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="22"></a><dl>
<dt><b>22</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the user account. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_22">USER_INFO_22</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1003"></a><dl>
<dt><b>1003</b></dt>
</dl>
</td>
<td width="60%">
Specifies a user password. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1003">USER_INFO_1003</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies a user privilege level. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1005">USER_INFO_1005</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1006"></a><dl>
<dt><b>1006</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path of the home directory for the user. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1006">USER_INFO_1006</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1007"></a><dl>
<dt><b>1007</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment to associate with the user account. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1007">USER_INFO_1007</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1008"></a><dl>
<dt><b>1008</b></dt>
</dl>
</td>
<td width="60%">
Specifies user account attributes. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008">USER_INFO_1008</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1009"></a><dl>
<dt><b>1009</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path for the user's logon script file. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1009">USER_INFO_1009</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1010"></a><dl>
<dt><b>1010</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user's operator privileges. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1010">USER_INFO_1010</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1011"></a><dl>
<dt><b>1011</b></dt>
</dl>
</td>
<td width="60%">
Specifies the full name of the user. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1011">USER_INFO_1011</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1012"></a><dl>
<dt><b>1012</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment to associate with the user. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1012">USER_INFO_1012</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1014"></a><dl>
<dt><b>1014</b></dt>
</dl>
</td>
<td width="60%">
Specifies the names of workstations from which the user can log on. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1014">USER_INFO_1014</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1017"></a><dl>
<dt><b>1017</b></dt>
</dl>
</td>
<td width="60%">
Specifies when the user account expires. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1017">USER_INFO_1017</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1020"></a><dl>
<dt><b>1020</b></dt>
</dl>
</td>
<td width="60%">
Specifies the times during which the user can log on. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1020">USER_INFO_1020</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1024"></a><dl>
<dt><b>1024</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user's country/region code. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1024">USER_INFO_1024</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1051"></a><dl>
<dt><b>1051</b></dt>
</dl>
</td>
<td width="60%">
Specifies the relative identifier of a global group that represents the enrolled user. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1051">USER_INFO_1051</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1052"></a><dl>
<dt><b>1052</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path to a network user's profile. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1052">USER_INFO_1052</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1053"></a><dl>
<dt><b>1053</b></dt>
</dl>
</td>
<td width="60%">
Specifies the drive letter assigned to the user's home directory. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1053">USER_INFO_1053</a> structure.

</td>
</tr>
</table>

### -param buf [in]

A pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

A pointer to a value that receives the index of the first member of the user information structure that causes ERROR_INVALID_PARAMETER. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NotPrimary</b></dt>
</dl>
</td>
<td width="60%">
The operation is allowed only on the primary domain controller of the domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SpeGroupOp</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed on specified special groups, which are user groups, admin groups, local groups, or guest groups.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_LastAdmin</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed on the last administrative account.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BadPassword</b></dt>
</dl>
</td>
<td width="60%">
The share name or password is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_PasswordTooShort</b></dt>
</dl>
</td>
<td width="60%">
The password is shorter than required. (The password could also be too long, be too recent in its change history, not have enough unique characters, or not meet another password policy requirement.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

</td>
</tr>
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function.

Only users or applications having administrative privileges can call the 
<b>NetUserSetInfo</b> function to change a user's password. When an administrator calls 
<b>NetUserSetInfo</b>, the only restriction applied is that the new password length must be consistent with system modals. A user or application that knows a user's current password can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword">NetUserChangePassword</a> function to change the password. For more information about calling functions that require administrator privileges, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Members of the Administrators local group can set any modifiable user account elements. All users can set the <b>usri2_country_code</b> member of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_2">USER_INFO_2</a> structure (and the <b>usri1024_country_code</b> member of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1024">USER_INFO_1024</a> structure) for their own accounts.

A member of the Account Operator's local group cannot set details for an Administrators class account, give an existing account Administrator privilege, or change the operator privilege of any account. If you attempt to change the privilege level or disable the last account with Administrator privilege in the security database, (the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory), the 
<b>NetUserSetInfo</b> function fails and returns NERR_LastAdmin.

To set the following user account control flags, the following <a href="/windows/desktop/SecAuthZ/privileges">privileges</a> and <a href="/windows/desktop/AD/control-access-rights">control access rights</a> are required.

<table>
<tr>
<th>Account control flag</th>
<th>Privilege or right required</th>
</tr>
<tr>
<td>UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</td>
<td>SeEnableDelegationPrivilege privilege, which is granted to Administrators by default. </td>
</tr>
<tr>
<td>UF_TRUSTED_FOR_DELEGATION</td>
<td>SeEnableDelegationPrivilege.</td>
</tr>
<tr>
<td>UF_PASSWD_NOTREQD</td>
<td>"Update password not required" control access right on the Domain object, which is granted to authenticated users by default.</td>
</tr>
<tr>
<td>UF_DONT_EXPIRE_PASSWD</td>
<td>"Unexpire password" control access right on the Domain object, which is granted to authenticated users by default.</td>
</tr>
<tr>
<td>UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</td>
<td>"Enable per user reversibly encrypted password" control access right on the Domain object, which is granted to authenticated users by default.</td>
</tr>
<tr>
<td>UF_SERVER_TRUST_ACCOUNT</td>
<td>"Add/remove replica in domain" control access right on the Domain object, which is granted to Administrators by default.</td>
</tr>
</table>
 

For a list of privilege constants, see <a href="/windows/desktop/SecAuthZ/authorization-constants">Authorization  Constants</a>.

The correct way to specify the new name for an account is to call 
<b>NetUserSetInfo</b> with 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_0">USER_INFO_0</a> and to specify the new value using the <b>usri0_name</b> member. If you call 
<b>NetUserSetInfo</b> with other information levels and specify a value using a <b>usriX_name</b> member, the value is ignored.

Note that calls to 
<b>NetUserSetInfo</b> can change the home directory only for user accounts that the network server creates.

If the 
<b>NetUserSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the first member of the user information structure that is invalid. (A user information structure begins with USER_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix usri*_ indicates that the member can begin with multiple prefixes, for example, usri10_ or usri1003_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>USER_NAME_PARMNUM</td>
<td>usri*_name</td>
</tr>
<tr>
<td>USER_PASSWORD_PARMNUM</td>
<td>usri*_password</td>
</tr>
<tr>
<td>USER_PASSWORD_AGE_PARMNUM</td>
<td>usri*_password_age</td>
</tr>
<tr>
<td>USER_PRIV_PARMNUM</td>
<td>usri*_priv</td>
</tr>
<tr>
<td>USER_HOME_DIR_PARMNUM</td>
<td>usri*_home_dir</td>
</tr>
<tr>
<td>USER_COMMENT_PARMNUM</td>
<td>usri*_comment</td>
</tr>
<tr>
<td>USER_FLAGS_PARMNUM</td>
<td>usri*_flags</td>
</tr>
<tr>
<td>USER_SCRIPT_PATH_PARMNUM</td>
<td>usri*_script_path</td>
</tr>
<tr>
<td>USER_AUTH_FLAGS_PARMNUM</td>
<td>usri*_auth_flags</td>
</tr>
<tr>
<td>USER_FULL_NAME_PARMNUM</td>
<td>usri*_full_name</td>
</tr>
<tr>
<td>USER_USR_COMMENT_PARMNUM</td>
<td>usri*_usr_comment</td>
</tr>
<tr>
<td>USER_PARMS_PARMNUM</td>
<td>usri*_parms</td>
</tr>
<tr>
<td>USER_WORKSTATIONS_PARMNUM</td>
<td>usri*_workstations</td>
</tr>
<tr>
<td>USER_LAST_LOGON_PARMNUM</td>
<td>usri*_last_logon</td>
</tr>
<tr>
<td>USER_LAST_LOGOFF_PARMNUM</td>
<td>usri*_last_logoff</td>
</tr>
<tr>
<td>USER_ACCT_EXPIRES_PARMNUM</td>
<td>usri*_acct_expires</td>
</tr>
<tr>
<td>USER_MAX_STORAGE_PARMNUM</td>
<td>usri*_max_storage</td>
</tr>
<tr>
<td>USER_UNITS_PER_WEEK_PARMNUM</td>
<td>usri*_units_per_week</td>
</tr>
<tr>
<td>USER_LOGON_HOURS_PARMNUM</td>
<td>usri*_logon_hours</td>
</tr>
<tr>
<td>USER_PAD_PW_COUNT_PARMNUM</td>
<td>usri*_bad_pw_count</td>
</tr>
<tr>
<td>USER_NUM_LOGONS_PARMNUM</td>
<td>usri*_num_logons</td>
</tr>
<tr>
<td>USER_LOGON_SERVER_PARMNUM</td>
<td>usri*_logon_server</td>
</tr>
<tr>
<td>USER_COUNTRY_CODE_PARMNUM</td>
<td>usri*_country_code</td>
</tr>
<tr>
<td>USER_CODE_PAGE_PARMNUM</td>
<td>usri*_code_page</td>
</tr>
<tr>
<td>USER_PRIMARY_GROUP_PARMNUM</td>
<td>usri*_primary_group_id</td>
</tr>
<tr>
<td>USER_PROFILE_PARMNUM</td>
<td>usri*_profile</td>
</tr>
<tr>
<td>USER_HOME_DIR_DRIVE_PARMNUM</td>
<td>usri*_home_dir_drive</td>
</tr>
</table>
 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

The 
<b>NetUserSetInfo</b> function does not control how the password parameters are secured when sent over the network to a remote server to change a user password. Any encryption of these parameters is handled by the Remote Procedure Call (RPC) mechanism supported by the network redirector that provides the network transport. Encryption is also controlled  by the security mechanisms supported by the local computer and the security mechanisms supported by remote network server specified in the <i>servername</i>   parameter. For more details on security when the Microsoft network redirector is used and the remote network server is running Microsoft Windows, see the protocol documentation for <a href="/openspecs/windows_protocols/ms-rpce/290c38b1-92fe-4229-91e6-4fc376610c15">MS-RPCE</a> and <a href="/openspecs/windows_protocols/ms-samr/4df07fab-1bbc-452f-8e92-7853a3c7e380">MS-SAMR</a>.


#### Examples

The following code sample demonstrates how to disable a user account with a call to the 
<b>NetUserSetInfo</b> function. The code sample fills in the <b>usri1008_flags</b> member of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008">USER_INFO_1008</a> structure, specifying the value UF_ACCOUNTDISABLE. Then the sample calls 
<b>NetUserSetInfo</b>, specifying information level 0.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwLevel = 1008;
   USER_INFO_1008 ui;
   NET_API_STATUS nStatus;

   if (argc != 3)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName\n", argv[0]);
      exit(1);
   }
   // Fill in the USER_INFO_1008 structure member.
   // UF_SCRIPT: required.
   //
   ui.usri1008_flags = UF_SCRIPT | UF_ACCOUNTDISABLE;
   //
   // Call the NetUserSetInfo function 
   //  to disable the account, specifying level 1008.
   //
   nStatus = NetUserSetInfo(argv[1],
                            argv[2],
                            dwLevel,
                            (LPBYTE)&ui,
                            NULL);
   //
   // Display the result of the call.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"User account %s has been disabled\n", argv[2]);
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_0">USER_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1003">USER_INFO_1003</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1005">USER_INFO_1005</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1006">USER_INFO_1006</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1007">USER_INFO_1007</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008">USER_INFO_1008</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1009">USER_INFO_1009</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1010">USER_INFO_1010</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1011">USER_INFO_1011</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1012">USER_INFO_1012</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1013">USER_INFO_1013</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1014">USER_INFO_1014</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1017">USER_INFO_1017</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1020">USER_INFO_1020</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1024">USER_INFO_1024</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1051">USER_INFO_1051</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1052">USER_INFO_1052</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1053">USER_INFO_1053</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_2">USER_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_21">USER_INFO_21</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_22">USER_INFO_22</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_4">USER_INFO_4</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>