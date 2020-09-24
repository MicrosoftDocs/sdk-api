---
UID: NF:lmaccess.NetUserAdd
title: NetUserAdd function (lmaccess.h)
description: The NetUserAdd function adds a user account and assigns a password and privilege level.
helpviewer_keywords: ["1","2","3","4","NetUserAdd","NetUserAdd function [Network Management]","_win32_netuseradd","lmaccess/NetUserAdd","netmgmt.netuseradd"]
old-location: netmgmt\netuseradd.htm
tech.root: NetMgmt
ms.assetid: b5ca5f76-d40b-4abf-925a-0de54fc476e4
ms.date: 12/05/2018
ms.keywords: 1, 2, 3, 4, NetUserAdd, NetUserAdd function [Network Management], _win32_netuseradd, lmaccess/NetUserAdd, netmgmt.netuseradd
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
 - NetUserAdd
 - lmaccess/NetUserAdd
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
 - NetUserAdd
---

# NetUserAdd function


## -description

The
				<b>NetUserAdd</b> function adds a user account and assigns a password and privilege level.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the user account. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a> structure. 




When you specify this level, the call initializes certain attributes to their default values. For more information, see the following Remarks section.

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

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the user information structure that causes ERROR_INVALID_PARAMETER. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

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
<dt><b>NERR_GroupExists</b></dt>
</dl>
</td>
<td width="60%">
The group already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserExists</b></dt>
</dl>
</td>
<td width="60%">
The user account already exists.

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
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsuser">IADsUser</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the user container is used to perform the access check for this function. The caller must be able to create child objects of the user class.

Server users must use a system in which the server creates a system account for the new user. The creation of this account is controlled by several parameters in the server's LanMan.ini file.

If the newly added user already exists as a system user, the <b>usri1_home_dir</b> member of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a> structure is ignored.

When you call the 
<b>NetUserAdd</b> function and specify information level 1, the call initializes the additional members in the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_2">USER_INFO_2</a>, 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3">USER_INFO_3</a>, and 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_4">USER_INFO_4</a> structures to their default values. You can change the default values by making subsequent calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function. The default values supplied are listed following. (The prefix usriX indicates that the member can begin with multiple prefixes, for example, usri2_ or usri4_.)

<table>
<tr>
<th>Member</th>
<th>Default Value</th>
</tr>
<tr>
<td>usriX_auth_flags</td>
<td>None (0)</td>
</tr>
<tr>
<td>usriX_full_name</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_usr_comment</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_parms</td>
<td>None (null string)</td>
</tr>
<tr>
<td>usriX_workstations</td>
<td>All (null string)</td>
</tr>
<tr>
<td>usriX_acct_expires</td>
<td>Never (TIMEQ_FOREVER)</td>
</tr>
<tr>
<td>usriX_max_storage</td>
<td>Unlimited (USER_MAXSTORAGE_UNLIMITED)</td>
</tr>
<tr>
<td>usriX_logon_hours</td>
<td>Logon allowed at any time (each element 0xFF; all bits set to 1)</td>
</tr>
<tr>
<td>usriX_logon_server</td>
<td>Any domain controller (\\*)</td>
</tr>
<tr>
<td>usriX_country_code</td>
<td>0</td>
</tr>
<tr>
<td>usriX_code_page</td>
<td>0</td>
</tr>
</table>
 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to add a user account and assign a privilege level using a call to the 
<b>NetUserAdd</b> function. The code sample fills in the members of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a> structure and calls 
<b>NetUserAdd</b>, specifying information level 1.


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
   USER_INFO_1 ui;
   DWORD dwLevel = 1;
   DWORD dwError = 0;
   NET_API_STATUS nStatus;

   if (argc != 3)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName\n", argv[0]);
      exit(1);
   }
   //
   // Set up the USER_INFO_1 structure.
   //  USER_PRIV_USER: name identifies a user, 
   //    rather than an administrator or a guest.
   //  UF_SCRIPT: required 
   //
   ui.usri1_name = argv[2];
   ui.usri1_password = argv[2];
   ui.usri1_priv = USER_PRIV_USER;
   ui.usri1_home_dir = NULL;
   ui.usri1_comment = NULL;
   ui.usri1_flags = UF_SCRIPT;
   ui.usri1_script_path = NULL;
   //
   // Call the NetUserAdd function, specifying level 1.
   //
   nStatus = NetUserAdd(argv[1],
                        dwLevel,
                        (LPBYTE)&ui,
                        &dwError);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"User %s has been successfully added on %s\n",
               argv[2], argv[1]);
   //
   // Otherwise, print the system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel">NetUserDel</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1">USER_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_2">USER_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-user_info_4">USER_INFO_4</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>