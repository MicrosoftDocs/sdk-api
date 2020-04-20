---
UID: NF:lmaccess.NetLocalGroupDelMembers
title: NetLocalGroupDelMembers function (lmaccess.h)
description: The NetLocalGroupDelMembers function removes one or more members from an existing local group. Local group members can be users or global groups.helpviewer_keywords: ["0","3","NetLocalGroupDelMembers","NetLocalGroupDelMembers function [Network Management]","_win32_netlocalgroupdelmembers","lmaccess/NetLocalGroupDelMembers","netmgmt.netlocalgroupdelmembers"]
old-location: netmgmt\netlocalgroupdelmembers.htm
tech.root: NetMgmt
ms.assetid: 85ae796b-c94a-46a8-9fa8-6c612db38671
ms.date: 12/05/2018
ms.keywords: 0, 3, NetLocalGroupDelMembers, NetLocalGroupDelMembers function [Network Management], _win32_netlocalgroupdelmembers, lmaccess/NetLocalGroupDelMembers, netmgmt.netlocalgroupdelmembers
f1_keywords:
- lmaccess/NetLocalGroupDelMembers
dev_langs:
- c++
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
- NetLocalGroupDelMembers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetLocalGroupDelMembers function


## -description


The 
				<b>NetLocalGroupDelMembers</b> function removes one or more members from an existing local group. Local group members can be users or global groups.


## -parameters




### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param groupname [in]

Pointer to a constant string that specifies the name of the local group from which the specified users or global groups will be removed. For more information, see the following Remarks section.


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
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-identifiers">security identifier</a> (SID) of a local group member to remove. The <i>buf</i> parameter points to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Specifies the domain and name of a local group member to remove. The <i>buf</i> parameter points to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a> structures.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to a buffer that specifies the members to be removed. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.


### -param totalentries [in]

Specifies the number of entries in the array pointed to by the <i>buf</i> parameter.


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
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The local group specified by the <i>groupname</i> parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified members do not exist. No members were deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEMBER_NOT_IN_ALIAS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the members specified were not members of the local group. No members were deleted.

</td>
</tr>
</table>
 




## -remarks



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/local-group-functions">Local Group
		  Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmembers">NetLocalGroupAddMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdel">NetLocalGroupDel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>
 

 

