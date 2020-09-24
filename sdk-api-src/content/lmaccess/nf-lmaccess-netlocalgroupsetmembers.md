---
UID: NF:lmaccess.NetLocalGroupSetMembers
title: NetLocalGroupSetMembers function (lmaccess.h)
description: The NetLocalGroupSetMembers function sets the membership for the specified local group.
helpviewer_keywords: ["0","3","NetLocalGroupSetMembers","NetLocalGroupSetMembers function [Network Management]","_win32_netlocalgroupsetmembers","lmaccess/NetLocalGroupSetMembers","netmgmt.netlocalgroupsetmembers"]
old-location: netmgmt\netlocalgroupsetmembers.htm
tech.root: NetMgmt
ms.assetid: 4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c
ms.date: 12/05/2018
ms.keywords: 0, 3, NetLocalGroupSetMembers, NetLocalGroupSetMembers function [Network Management], _win32_netlocalgroupsetmembers, lmaccess/NetLocalGroupSetMembers, netmgmt.netlocalgroupsetmembers
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
 - NetLocalGroupSetMembers
 - lmaccess/NetLocalGroupSetMembers
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
 - NetLocalGroupSetMembers
---

# NetLocalGroupSetMembers function


## -description

The 
				<b>NetLocalGroupSetMembers</b> function sets the membership for the specified local group. Each user or global group specified is made a member of the local group. Users or global groups that are not specified but who are currently members of the local group will have their membership revoked.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

Pointer to a constant string that specifies the name of the local group in which the specified users or global groups should be granted membership. For more information, see the following Remarks section.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



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
Specifies the 
<a href="/windows/desktop/SecAuthZ/security-identifiers">security identifier</a> (SID) associated with a local group member. The <i>buf</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies the account and domain names of the local group member. The <i>buf</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a> structures.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that contains the member information. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param totalentries [in]

Specifies a value that contains the total number of entries in the buffer pointed to by the <i>buf</i> parameter.

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
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The group specified by the <i>groupname</i> parameter does not exist.

</td>
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
<dt><b>ERROR_NO_SUCH_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the members doesn't exist. The local group membership was not changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the members cannot be added because it has an invalid account type. The local group membership was not changed.

</td>
</tr>
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function.

You can replace the local group membership with an entirely new list of members by calling the 
<b>NetLocalGroupSetMembers</b> function. The typical sequence of steps to perform this follows.

<p class="proch"><b>To replace the local group membership</b>

<ol>
<li>Call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a> function to retrieve the current membership list.</li>
<li>Modify the returned membership list to reflect the new membership.</li>
<li>Call the 
<b>NetLocalGroupSetMembers</b> function to replace the old membership list with the new membership list.</li>
</ol>
To add one or more existing user accounts or global group accounts to an existing local group, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmembers">NetLocalGroupAddMembers</a> function. To remove one or more members from an existing local group, call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmembers">NetLocalGroupDelMembers</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group
		  Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmembers">NetLocalGroupAddMembers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmembers">NetLocalGroupDelMembers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>