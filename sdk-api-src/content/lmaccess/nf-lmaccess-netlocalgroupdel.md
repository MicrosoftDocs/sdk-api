---
UID: NF:lmaccess.NetLocalGroupDel
title: NetLocalGroupDel function (lmaccess.h)
description: The NetLocalGroupDel function deletes a local group account and all its members from the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["NetLocalGroupDel","NetLocalGroupDel function [Network Management]","_win32_netlocalgroupdel","lmaccess/NetLocalGroupDel","netmgmt.netlocalgroupdel"]
old-location: netmgmt\netlocalgroupdel.htm
tech.root: NetMgmt
ms.assetid: b26bfd52-c20a-4f6f-9503-87cac5168362
ms.date: 12/05/2018
ms.keywords: NetLocalGroupDel, NetLocalGroupDel function [Network Management], _win32_netlocalgroupdel, lmaccess/NetLocalGroupDel, netmgmt.netlocalgroupdel
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
 - NetLocalGroupDel
 - lmaccess/NetLocalGroupDel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - Samcli.dll
api_name:
 - NetLocalGroupDel
---

# NetLocalGroupDel function


## -description

The
				<b>NetLocalGroupDel</b> function deletes a local group account and all its members from the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param groupname [in]

Pointer to a constant string that specifies the name of the local group account to delete. For more information, see the following Remarks section.

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
The local group specified by the <i>groupname</i> parameter does not exist.

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
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

## -see-also

<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group
		  Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupadd">NetLocalGroupAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmembers">NetLocalGroupDelMembers</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>