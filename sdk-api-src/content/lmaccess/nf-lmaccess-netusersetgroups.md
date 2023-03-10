---
UID: NF:lmaccess.NetUserSetGroups
title: NetUserSetGroups function (lmaccess.h)
description: The NetUserSetGroups function sets global group memberships for a specified user account.
helpviewer_keywords: ["0","1","NetUserSetGroups","NetUserSetGroups function [Network Management]","_win32_netusersetgroups","lmaccess/NetUserSetGroups","netmgmt.netusersetgroups"]
old-location: netmgmt\netusersetgroups.htm
tech.root: NetMgmt
ms.assetid: 7042c43a-09d1-4179-8074-eb055dc279a6
ms.date: 12/05/2018
ms.keywords: 0, 1, NetUserSetGroups, NetUserSetGroups function [Network Management], _win32_netusersetgroups, lmaccess/NetUserSetGroups, netmgmt.netusersetgroups
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
 - NetUserSetGroups
 - lmaccess/NetUserSetGroups
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
 - NetUserSetGroups
---

# NetUserSetGroups function


## -description

The
				<b>NetUserSetGroups</b> function sets global group memberships for a specified user account.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param username [in]

A pointer to a constant string that specifies the name of the user for which to set global group memberships. For more information, see the Remarks section.

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
The <i>buf</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a> structures that specifies global group names.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a> structures that specifies global group names with attributes.

</td>
</tr>
</table>

### -param buf [in]

A pointer to the buffer that specifies the data. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param num_entries [in]

The number of entries contained in the array pointed to by the <i>buf</i> parameter.

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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The system call level is not correct. This error is returned if the <i>level</i> parameter was specified as a value other than 0 or 1. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter passed was not valid. This error is returned if the <i>num_entries</i> parameter was not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available to complete the operation.

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
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The group group name specified by the <b>grui0_name</b> in the <a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a> structure or <b>grui1_name</b> member in the <a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a> structure pointed to by the <i>buf</i> parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InternalError</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred.

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

To grant a user membership in one existing global group, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.


#### Examples

The following code sample demonstrates how to set global group memberships for a user account with a call to the 
<b>NetUserSetGroups</b> function. The code sample fills in the <b>grui0_name</b> member of the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a> structure and calls 
<b>NetUserSetGroups</b>, specifying information level 0.


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
   DWORD dwLevel = 0;
   GROUP_USERS_INFO_0 gi;
   NET_API_STATUS nStatus;

   if (argc != 4)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName UserName GroupName\n", argv[0]);
      exit(1);
   }
   //
   // Fill in the GROUP_USERS_INFO_0 structure member.
   //
   gi.grui0_name = argv[3];
   //
   // Call the NetUserSetGroups function; specify level 0.
   //
   nStatus = NetUserSetGroups(argv[1],
                              argv[2],
                              dwLevel,
                              (LPBYTE)&gi,
                              1);
   //
   // If the call succeeds, inform the user.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"Group membership has been successful for %s\n", argv[2]);
   //
   // Otherwise, print the system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>