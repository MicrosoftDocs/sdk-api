---
UID: NF:lmaccess.NetGroupGetUsers
title: NetGroupGetUsers function (lmaccess.h)
description: The NetGroupGetUsers function retrieves a list of the members in a particular global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","NetGroupGetUsers","NetGroupGetUsers function [Network Management]","_win32_netgroupgetusers","lmaccess/NetGroupGetUsers","netmgmt.netgroupgetusers"]
old-location: netmgmt\netgroupgetusers.htm
tech.root: NetMgmt
ms.assetid: a9bcb806-f44c-4db2-9644-06687b31405d
ms.date: 12/05/2018
ms.keywords: 0, 1, NetGroupGetUsers, NetGroupGetUsers function [Network Management], _win32_netgroupgetusers, lmaccess/NetGroupGetUsers, netmgmt.netgroupgetusers
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
 - NetGroupGetUsers
 - lmaccess/NetGroupGetUsers
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
 - NetGroupGetUsers
---

# NetGroupGetUsers function


## -description

The
				<b>NetGroupGetUsers</b> function retrieves a list of the members in a particular global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

A pointer to a constant string that specifies the name of the global group whose members are to be listed. For more information, see the following Remarks section.

### -param level [in]

The information level of the data requested. This parameter can be one of the following values. 



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
Return the global group's member names. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the global group's member names and attributes. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

A pointer to the address of the buffer that receives the information structure. The system allocates the memory for this buffer. You must call the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function to deallocate the memory. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

The preferred maximum length of the returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required to hold the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position.

### -param ResumeHandle [in, out]

A pointer to a variable that contains a resume handle that is used to continue an existing user enumeration. The handle should be zero on the first call and left unchanged for subsequent calls. If <i>ResumeHandle</i> parameter is <b>NULL</b>, no resume handle is stored.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

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
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The global group name in the structure pointed to by <i>bufptr</i> parameter could not be found.

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
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Group object is used to perform the access check for this function.

To grant one user membership in an existing global group, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a> function. To remove a user from a global group, call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdeluser">NetGroupDelUser</a> function. For information about replacing the membership of a global group, see 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetusers">NetGroupSetUsers</a>.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_0">GROUP_USERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a>



<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdeluser">NetGroupDelUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetusers">NetGroupSetUsers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>