---
UID: NF:lmaccess.NetLocalGroupSetInfo
title: NetLocalGroupSetInfo function (lmaccess.h)
description: The NetLocalGroupSetInfo function changes the name of an existing local group. The function also associates a comment with a local group.
helpviewer_keywords: ["0","1","1002","NetLocalGroupSetInfo","NetLocalGroupSetInfo function [Network Management]","_win32_netlocalgroupsetinfo","lmaccess/NetLocalGroupSetInfo","netmgmt.netlocalgroupsetinfo"]
old-location: netmgmt\netlocalgroupsetinfo.htm
tech.root: NetMgmt
ms.assetid: c1d2a68b-0910-4815-9547-0f0f3c983164
ms.date: 12/05/2018
ms.keywords: 0, 1, 1002, NetLocalGroupSetInfo, NetLocalGroupSetInfo function [Network Management], _win32_netlocalgroupsetinfo, lmaccess/NetLocalGroupSetInfo, netmgmt.netlocalgroupsetinfo
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
 - NetLocalGroupSetInfo
 - lmaccess/NetLocalGroupSetInfo
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
 - NetLocalGroupSetInfo
---

# NetLocalGroupSetInfo function


## -description

The 
				<b>NetLocalGroupSetInfo</b> function changes the name of an existing local group. The function also associates a comment with a local group.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

Pointer to a constant string that specifies the name of the local group account to modify. For more information, see the following Remarks section.

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
Specifies the local group name. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_0">LOCALGROUP_INFO_0</a> structure. Use this level to change the name of an existing local group.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies the local group name and a comment to associate with the group. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_1">LOCALGROUP_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1002"></a><dl>
<dt><b>1002</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment to associate with the local group. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_1002">LOCALGROUP_INFO_1002</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to a buffer that contains the local group information. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the local group information structure that caused the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.

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
<dt><b>ERROR_NO_SUCH_ALIAS</b></dt>
</dl>
</td>
<td width="60%">
The specified local group does not exist.

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
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is invalid.

</td>
</tr>
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function. Typically, callers must have write access to the entire object for calls to this function to succeed.

To specify the new name of an existing local group, call 
<b>NetLocalGroupSetInfo</b> with 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_0">LOCALGROUP_INFO_0</a> and specify a value using the <b>lgrpi0_name</b> member. If you call the 
<b>NetLocalGroupSetInfo</b> function with 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_1">LOCALGROUP_INFO_1</a> and specify a new value using the <b>lgrpi1_name</b> member, that value will be ignored.

If the 
<b>NetLocalGroupSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the first member of the local group information structure that is invalid. (A local group information structure begins with LOCALGROUP_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix lgrpi*_ indicates that the member can begin with multiple prefixes, for example, lgrpi0_ or lgrpi1_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>LOCALGROUP_NAME_PARMNUM</td>
<td>lgrpi*_name</td>
</tr>
<tr>
<td>LOCALGROUP_COMMENT_PARMNUM</td>
<td>lgrpi*_comment</td>
</tr>
</table>
 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_0">LOCALGROUP_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_1">LOCALGROUP_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_info_1002">LOCALGROUP_INFO_1002</a>



<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group
		  Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetinfo">NetLocalGroupGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>