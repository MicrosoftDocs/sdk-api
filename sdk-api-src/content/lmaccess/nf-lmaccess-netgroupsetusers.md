---
UID: NF:lmaccess.NetGroupSetUsers
title: NetGroupSetUsers function (lmaccess.h)
description: The NetGroupSetUsers function sets the membership for the specified global group.
helpviewer_keywords: ["0","1","NetGroupSetUsers","NetGroupSetUsers function [Network Management]","_win32_netgroupsetusers","lmaccess/NetGroupSetUsers","netmgmt.netgroupsetusers"]
old-location: netmgmt\netgroupsetusers.htm
tech.root: NetMgmt
ms.assetid: 4221f5c8-a71c-4368-9be4-9562063b6cfd
ms.date: 12/05/2018
ms.keywords: 0, 1, NetGroupSetUsers, NetGroupSetUsers function [Network Management], _win32_netgroupsetusers, lmaccess/NetGroupSetUsers, netmgmt.netgroupsetusers
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
 - NetGroupSetUsers
 - lmaccess/NetGroupSetUsers
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
 - NetGroupSetUsers
---

# NetGroupSetUsers function


## -description

The
				<b>NetGroupSetUsers</b> function sets the membership for the specified global group. Each user you specify is enrolled as a member of the global group. Users you do not specify, but who are currently members of the global group, will have their membership revoked.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

A pointer to a constant string that specifies the name of the global group of interest. For more information, see the Remarks section.

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
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a> structures that specify user names.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a> structures that specifies user names and the attributes of the group.

</td>
</tr>
</table>

### -param buf [in]

A pointer to the buffer that contains the data. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param totalentries [in]

The number of entries in the buffer pointed to by the <i>buf</i> parameter.

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
A parameter passed was not valid. This error is returned if the <i>totalentries</i> parameter was not valid. 

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
The global group name could not be found.

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
<dt><b>NERR_SpeGroupOp</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed on certain special groups. These groups include user groups, admin groups, local groups, and guest groups.

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

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Group object is used to perform the access check for this function.

You can replace the global group membership with an entirely new list of members by calling the 
<b>NetGroupSetUsers</b> function. The typical sequence of steps to perform this follows.

<p class="proch"><b>To replace the global group membership</b>

<ol>
<li>Call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetusers">NetGroupGetUsers</a> function to retrieve the current membership list.</li>
<li>Modify the returned membership list to reflect the new membership.</li>
<li>Call the 
<b>NetGroupSetUsers</b> function to replace the old membership list with the new membership list.</li>
</ol>
To grant one user membership in an existing global group, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a> function. To remove a user from a global group, call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdeluser">NetGroupDelUser</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a>



<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdeluser">NetGroupDelUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetusers">NetGroupGetUsers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetgroups">NetUserSetGroups</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>