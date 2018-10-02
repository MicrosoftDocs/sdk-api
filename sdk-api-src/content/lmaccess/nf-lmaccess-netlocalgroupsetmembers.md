---
UID: NF:lmaccess.NetLocalGroupSetMembers
title: NetLocalGroupSetMembers function
author: windows-sdk-content
description: The NetLocalGroupSetMembers function sets the membership for the specified local group.
old-location: netmgmt\netlocalgroupsetmembers.htm
tech.root: NetMgmt
ms.assetid: 4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0, 3, NetLocalGroupSetMembers, NetLocalGroupSetMembers function [Network Management], _win32_netlocalgroupsetmembers, lmaccess/NetLocalGroupSetMembers, netmgmt.netlocalgroupsetmembers
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
 - NetLocalGroupSetMembers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/library/Aa379571(v=VS.85).aspx">security identifier</a> (SID) associated with a local group member. The <i>buf</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies the account and domain names of the local group member. The <i>buf</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3</a> structures.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to the buffer that contains the member information. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


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



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function.

You can replace the local group membership with an entirely new list of members by calling the 
<b>NetLocalGroupSetMembers</b> function. The typical sequence of steps to perform this follows.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To replace the local group membership</b>

<ol>
<li>Call the 
<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a> function to retrieve the current membership list.</li>
<li>Modify the returned membership list to reflect the new membership.</li>
<li>Call the 
<b>NetLocalGroupSetMembers</b> function to replace the old membership list with the new membership list.</li>
</ol>
To add one or more existing user accounts or global group accounts to an existing local group, you can call the 
<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a> function. To remove one or more members from an existing local group, call the 
<a href="https://msdn.microsoft.com/85ae796b-c94a-46a8-9fa8-6c612db38671">NetLocalGroupDelMembers</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.




## -see-also




<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group
		  Functions</a>



<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a>



<a href="https://msdn.microsoft.com/85ae796b-c94a-46a8-9fa8-6c612db38671">NetLocalGroupDelMembers</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

