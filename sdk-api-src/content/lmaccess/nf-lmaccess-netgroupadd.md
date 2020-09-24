---
UID: NF:lmaccess.NetGroupAdd
title: NetGroupAdd function (lmaccess.h)
description: The NetGroupAdd function creates a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","2","3","NetGroupAdd","NetGroupAdd function [Network Management]","_win32_netgroupadd","lmaccess/NetGroupAdd","netmgmt.netgroupadd"]
old-location: netmgmt\netgroupadd.htm
tech.root: NetMgmt
ms.assetid: fbf90758-79fd-4959-b6d0-ad3872e77242
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, NetGroupAdd, NetGroupAdd function [Network Management], _win32_netgroupadd, lmaccess/NetGroupAdd, netmgmt.netgroupadd
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
 - NetGroupAdd
 - lmaccess/NetGroupAdd
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
 - NetGroupAdd
---

# NetGroupAdd function


## -description

The
				<b>NetGroupAdd</b> function creates a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

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
Specifies a global group name. The <i>buf</i> parameter contains a pointer to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies a global group name and a comment. The <i>buf</i> parameter contains a pointer to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the global group. The <i>buf</i> parameter contains a pointer to a 
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
 Specifies detailed information about the global group. The <i>buf</i> parameter contains a pointer to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> structure.

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
</table>

### -param buf [in]

Pointer to a buffer that contains the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the global group information structure in error when ERROR_INVALID_PARAMETER is returned. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a> function.

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
<dt><b>NERR_GroupExists</b></dt>
</dl>
</td>
<td width="60%">
The global group already exists.

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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

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

The security descriptor of the user container is used to perform the access check for this function. The caller must be able to create child objects of the group class. Typically, callers must also have write access to the entire object for calls to this function to succeed.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a>



<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadduser">NetGroupAddUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdel">NetGroupDel</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupdeluser">NetGroupDelUser</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>