---
UID: NF:lmaccess.NetUserSetInfo
title: NetUserSetInfo function
author: windows-sdk-content
description: The NetUserSetInfo function sets the parameters of a user account.
old-location: netmgmt\netusersetinfo.htm
tech.root: netmgmt
ms.assetid: ffe49d4b-e7e8-4982-8087-59bb7534b257
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, 1, 1003, 1005, 1006, 1007, 1008, 1009, 1010, 1011, 1012, 1014, 1017, 1020, 1024, 1051, 1052, 1053, 2, 21, 22, 3, 4, NetUserSetInfo, NetUserSetInfo function [Network Management], _win32_netusersetinfo, lmaccess/NetUserSetInfo, netmgmt.netusersetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetUserSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a> structure. Use this structure to specify a new group name. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies level one information and additional attributes about the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a> structure. Note that  it is recommended that you use 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
 Specifies level two information and additional attributes about the user account. This level is valid only on servers. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="21"></a><dl>
<dt><b>21</b></dt>
</dl>
</td>
<td width="60%">
Specifies a one-way encrypted LAN Manager 2.<i>x</i>-compatible password. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/227e97c5-972e-4d4a-9609-53e60e76d43e">USER_INFO_21</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="22"></a><dl>
<dt><b>22</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/ff8d2088-953b-4a8a-bdcb-86148dc66a7a">USER_INFO_22</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1003"></a><dl>
<dt><b>1003</b></dt>
</dl>
</td>
<td width="60%">
Specifies a user password. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/ef1d1ecd-7226-4e4e-a0b3-ec096d3b1207">USER_INFO_1003</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies a user privilege level. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/a953b48f-bda0-4dce-a153-d4db912de533">USER_INFO_1005</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1006"></a><dl>
<dt><b>1006</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path of the home directory for the user. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/9eb4973b-cda5-4862-b558-3af90b7de19f">USER_INFO_1006</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1007"></a><dl>
<dt><b>1007</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment to associate with the user account. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/a2e49802-799d-4f98-aa6d-5cb1478cb4d4">USER_INFO_1007</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1008"></a><dl>
<dt><b>1008</b></dt>
</dl>
</td>
<td width="60%">
Specifies user account attributes. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/142408ef-ed8e-4af3-8fc2-ffdd40ce4f1e">USER_INFO_1008</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1009"></a><dl>
<dt><b>1009</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path for the user's logon script file. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/baaabbf9-9571-49db-bf38-a3fc2d0a200a">USER_INFO_1009</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1010"></a><dl>
<dt><b>1010</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user's operator privileges. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/6760729a-1d59-430e-8412-1257977af169">USER_INFO_1010</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1011"></a><dl>
<dt><b>1011</b></dt>
</dl>
</td>
<td width="60%">
Specifies the full name of the user. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/f60075b4-19c5-4998-b8c3-61e960e76035">USER_INFO_1011</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1012"></a><dl>
<dt><b>1012</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment to associate with the user. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/92501552-7afe-4a95-980a-576254a122a9">USER_INFO_1012</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1014"></a><dl>
<dt><b>1014</b></dt>
</dl>
</td>
<td width="60%">
Specifies the names of workstations from which the user can log on. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/ff7f385d-bcda-4560-b22f-d1fc94e7ae41">USER_INFO_1014</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1017"></a><dl>
<dt><b>1017</b></dt>
</dl>
</td>
<td width="60%">
Specifies when the user account expires. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/67ded50e-ab9a-4202-9496-1a39d1af0f58">USER_INFO_1017</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1020"></a><dl>
<dt><b>1020</b></dt>
</dl>
</td>
<td width="60%">
Specifies the times during which the user can log on. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/959ed1f4-d5ee-4d77-abd7-bb681778f0b1">USER_INFO_1020</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1024"></a><dl>
<dt><b>1024</b></dt>
</dl>
</td>
<td width="60%">
Specifies the user's country/region code. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/8133238f-c968-4a65-a8dd-7b9a61a193f5">USER_INFO_1024</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1051"></a><dl>
<dt><b>1051</b></dt>
</dl>
</td>
<td width="60%">
Specifies the relative identifier of a global group that represents the enrolled user. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/dbd7c63b-c383-48dd-98f2-087f2b41fc52">USER_INFO_1051</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1052"></a><dl>
<dt><b>1052</b></dt>
</dl>
</td>
<td width="60%">
Specifies the path to a network user's profile. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/55ec6819-8558-413a-9a79-c2d59993163d">USER_INFO_1052</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1053"></a><dl>
<dt><b>1053</b></dt>
</dl>
</td>
<td width="60%">
Specifies the drive letter assigned to the user's home directory. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/687b2c35-344d-49db-a1e2-fb5c2b5db2d6">USER_INFO_1053</a> structure.

</td>
</tr>
</table>
 


### -param buf [in]

A pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


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
<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a> and 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the User object is used to perform the access check for this function.

Only users or applications having administrative privileges can call the 
<b>NetUserSetInfo</b> function to change a user's password. When an administrator calls 
<b>NetUserSetInfo</b>, the only restriction applied is that the new password length must be consistent with system modals. A user or application that knows a user's current password can call the 
<a href="https://msdn.microsoft.com/e3791756-3bd4-490b-983a-9687373d846b">NetUserChangePassword</a> function to change the password. For more information about calling functions that require administrator privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

Members of the Administrators local group can set any modifiable user account elements. All users can set the <b>usri2_country_code</b> member of the 
<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a> structure (and the <b>usri1024_country_code</b> member of the 
<a href="https://msdn.microsoft.com/8133238f-c968-4a65-a8dd-7b9a61a193f5">USER_INFO_1024</a> structure) for their own accounts.

A member of the Account Operator's local group cannot set details for an Administrators class account, give an existing account Administrator privilege, or change the operator privilege of any account. If you attempt to change the privilege level or disable the last account with Administrator privilege in the security database, (the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory), the 
<b>NetUserSetInfo</b> function fails and returns NERR_LastAdmin.

To set the following user account control flags, the following <a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">privileges</a> and <a href="https://msdn.microsoft.com/27ad74bd-ad87-422e-a4a2-02c0d51c4dd4">control access rights</a> are required.

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
 

For a list of privilege constants, see <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Authorization  Constants</a>.

The correct way to specify the new name for an account is to call 
<b>NetUserSetInfo</b> with 
<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a> and to specify the new value using the <b>usri0_name</b> member. If you call 
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
<b>NetUserSetInfo</b> function does not control how the password parameters are secured when sent over the network to a remote server to change a user password. Any encryption of these parameters is handled by the Remote Procedure Call (RPC) mechanism supported by the network redirector that provides the network transport. Encryption is also controlled  by the security mechanisms supported by the local computer and the security mechanisms supported by remote network server specified in the <i>servername</i>   parameter. For more details on security when the Microsoft network redirector is used and the remote network server is running Microsoft Windows, see the protocol documentation for <a href="http://go.microsoft.com/fwlink/p/?linkid=200126">MS-RPCE</a> and <a href=" http://go.microsoft.com/fwlink/p/?linkid=200128">MS-SAMR</a>.


#### Examples

The following code sample demonstrates how to disable a user account with a call to the 
<b>NetUserSetInfo</b> function. The code sample fills in the <b>usri1008_flags</b> member of the 
<a href="https://msdn.microsoft.com/142408ef-ed8e-4af3-8fc2-ffdd40ce4f1e">USER_INFO_1008</a> structure, specifying the value UF_ACCOUNTDISABLE. Then the sample calls 
<b>NetUserSetInfo</b>, specifying information level 0.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include &lt;stdio.h&gt;
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

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
                            (LPBYTE)&amp;ui,
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5d24a2dd-d1ee-4c97-8fbc-0b336313b60c">USER_INFO_0</a>



<a href="https://msdn.microsoft.com/f17a1aef-45f1-461f-975d-75221d08277c">USER_INFO_1</a>



<a href="https://msdn.microsoft.com/ef1d1ecd-7226-4e4e-a0b3-ec096d3b1207">USER_INFO_1003</a>



<a href="https://msdn.microsoft.com/a953b48f-bda0-4dce-a153-d4db912de533">USER_INFO_1005</a>



<a href="https://msdn.microsoft.com/9eb4973b-cda5-4862-b558-3af90b7de19f">USER_INFO_1006</a>



<a href="https://msdn.microsoft.com/a2e49802-799d-4f98-aa6d-5cb1478cb4d4">USER_INFO_1007</a>



<a href="https://msdn.microsoft.com/142408ef-ed8e-4af3-8fc2-ffdd40ce4f1e">USER_INFO_1008</a>



<a href="https://msdn.microsoft.com/baaabbf9-9571-49db-bf38-a3fc2d0a200a">USER_INFO_1009</a>



<a href="https://msdn.microsoft.com/6760729a-1d59-430e-8412-1257977af169">USER_INFO_1010</a>



<a href="https://msdn.microsoft.com/f60075b4-19c5-4998-b8c3-61e960e76035">USER_INFO_1011</a>



<a href="https://msdn.microsoft.com/92501552-7afe-4a95-980a-576254a122a9">USER_INFO_1012</a>



<a href="https://msdn.microsoft.com/7166201d-57e3-4288-ad15-392cc3733dc6">USER_INFO_1013</a>



<a href="https://msdn.microsoft.com/ff7f385d-bcda-4560-b22f-d1fc94e7ae41">USER_INFO_1014</a>



<a href="https://msdn.microsoft.com/67ded50e-ab9a-4202-9496-1a39d1af0f58">USER_INFO_1017</a>



<a href="https://msdn.microsoft.com/959ed1f4-d5ee-4d77-abd7-bb681778f0b1">USER_INFO_1020</a>



<a href="https://msdn.microsoft.com/8133238f-c968-4a65-a8dd-7b9a61a193f5">USER_INFO_1024</a>



<a href="https://msdn.microsoft.com/dbd7c63b-c383-48dd-98f2-087f2b41fc52">USER_INFO_1051</a>



<a href="https://msdn.microsoft.com/55ec6819-8558-413a-9a79-c2d59993163d">USER_INFO_1052</a>



<a href="https://msdn.microsoft.com/687b2c35-344d-49db-a1e2-fb5c2b5db2d6">USER_INFO_1053</a>



<a href="https://msdn.microsoft.com/50c78c6a-a08f-473b-929a-9528e618165f">USER_INFO_2</a>



<a href="https://msdn.microsoft.com/227e97c5-972e-4d4a-9609-53e60e76d43e">USER_INFO_21</a>



<a href="https://msdn.microsoft.com/ff8d2088-953b-4a8a-bdcb-86148dc66a7a">USER_INFO_22</a>



<a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

