---
UID: NF:lmaccess.NetGroupSetUsers
title: NetGroupSetUsers function (lmaccess.h)
author: windows-sdk-content
description: The NetGroupSetUsers function sets the membership for the specified global group.
old-location: netmgmt\netgroupsetusers.htm
tech.root: NetMgmt
ms.assetid: 4221f5c8-a71c-4368-9be4-9562063b6cfd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0, 1, NetGroupSetUsers, NetGroupSetUsers function [Network Management], _win32_netgroupsetusers, lmaccess/NetGroupSetUsers, netmgmt.netgroupsetusers
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
 - NetGroupSetUsers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a> structures that specify user names.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a> structures that specifies user names and the attributes of the group.

</td>
</tr>
</table>
 


### -param buf [in]

A pointer to the buffer that contains the data. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


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



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the Group object is used to perform the access check for this function.

You can replace the global group membership with an entirely new list of members by calling the 
<b>NetGroupSetUsers</b> function. The typical sequence of steps to perform this follows.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To replace the global group membership</b>

<ol>
<li>Call the 
<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a> function to retrieve the current membership list.</li>
<li>Modify the returned membership list to reflect the new membership.</li>
<li>Call the 
<b>NetGroupSetUsers</b> function to replace the old membership list with the new membership list.</li>
</ol>
To grant one user membership in an existing global group, you can call the 
<a href="https://msdn.microsoft.com/a2eefde8-29e3-4fa1-87db-c7f6d24b699d">NetGroupAddUser</a> function. To remove a user from a global group, call the 
<a href="https://msdn.microsoft.com/ab8ce12a-60c0-4d79-8894-4537c6568e15">NetGroupDelUser</a> function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.




## -see-also




<a href="https://msdn.microsoft.com/cc0e5d27-91f1-4640-bb80-e73899fabba9">GROUP_USERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a>



<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/a2eefde8-29e3-4fa1-87db-c7f6d24b699d">NetGroupAddUser</a>



<a href="https://msdn.microsoft.com/ab8ce12a-60c0-4d79-8894-4537c6568e15">NetGroupDelUser</a>



<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a>



<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a>



<a href="https://msdn.microsoft.com/7042c43a-09d1-4179-8074-eb055dc279a6">NetUserSetGroups</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

