---
UID: NF:lmaccess.NetGroupSetInfo
title: NetGroupSetInfo function (lmaccess.h)
description: The NetGroupSetInfo function sets the parameters of a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","1002","1005","2","3","NetGroupSetInfo","NetGroupSetInfo function [Network Management]","_win32_netgroupsetinfo","lmaccess/NetGroupSetInfo","netmgmt.netgroupsetinfo"]
old-location: netmgmt\netgroupsetinfo.htm
tech.root: NetMgmt
ms.assetid: 8c235f9a-095e-4108-9b93-008ffe9bc776
ms.date: 12/05/2018
ms.keywords: 0, 1, 1002, 1005, 2, 3, NetGroupSetInfo, NetGroupSetInfo function [Network Management], _win32_netgroupsetinfo, lmaccess/NetGroupSetInfo, netmgmt.netgroupsetinfo
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
 - NetGroupSetInfo
 - lmaccess/NetGroupSetInfo
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
 - NetGroupSetInfo
---

# NetGroupSetInfo function


## -description

The
				<b>NetGroupSetInfo</b> function sets the parameters of a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

Pointer to a constant string that specifies the name of the global group for which to set information. For more information, see the following Remarks section.

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
Specifies a global group name. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies a global group name and a comment. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the global group. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_2">GROUP_INFO_2</a> structure. Note that on Windows XP and later, it is recommended that you use 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Specifies detailed information about the global group. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> structure.

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="1002"></a><dl>
<dt><b>1002</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment only about the global group. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1002">GROUP_INFO_1002</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies global group attributes. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1005">GROUP_INFO_1005</a> structure.

</td>
</tr>
</table>
 

For more information, see the following Remarks section.

### -param buf [in]

Pointer to a buffer that contains the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the group information structure in error following an ERROR_INVALID_PARAMETER error code. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.

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
<dt><b>NERR_SpeGroupOp</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed on certain special groups. These groups include user groups, admin groups, local groups, and guest groups.

</td>
</tr>
</table>

## -remarks

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Group object is used to perform the access check for this function. Typically, callers must have write access to the entire object for calls to this function to succeed.

The correct way to set the new name of a global group is to call the 
<b>NetGroupSetInfo</b> function, using a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a> structure. Specify the new value in the <b>grpi0_name</b> member. If you use a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a> structure and specify the value in the <b>grpi1_name</b> member, the new name value is ignored.

If the 
<b>NetGroupSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the first member of the group information structure that is invalid. (A group information structure begins with GROUP_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix grpi*_ indicates that the member can begin with multiple prefixes, for example, grpi1_ or grpi2_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>GROUP_NAME_PARMNUM</td>
<td>grpi*_name</td>
</tr>
<tr>
<td>GROUP_COMMENT_PARMNUM</td>
<td>grpi*_comment</td>
</tr>
<tr>
<td>GROUP_ATTRIBUTES_PARMNUM</td>
<td>grpi*_attributes</td>
</tr>
</table>
 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1002">GROUP_INFO_1002</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1005">GROUP_INFO_1005</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a>



<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetinfo">NetGroupGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>