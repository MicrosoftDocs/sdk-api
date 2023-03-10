---
UID: NF:lmaccess.NetLocalGroupGetMembers
title: NetLocalGroupGetMembers function (lmaccess.h)
description: The NetLocalGroupGetMembers function retrieves a list of the members of a particular local group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["0","1","2","3","NetLocalGroupGetMembers","NetLocalGroupGetMembers function [Network Management]","_win32_netlocalgroupgetmembers","lmaccess/NetLocalGroupGetMembers","netmgmt.netlocalgroupgetmembers"]
old-location: netmgmt\netlocalgroupgetmembers.htm
tech.root: NetMgmt
ms.assetid: 35770b32-dae9-46f5-84e3-1c31ca22f708
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, NetLocalGroupGetMembers, NetLocalGroupGetMembers function [Network Management], _win32_netlocalgroupgetmembers, lmaccess/NetLocalGroupGetMembers, netmgmt.netlocalgroupgetmembers
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
 - NetLocalGroupGetMembers
 - lmaccess/NetLocalGroupGetMembers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - samcli.dll
api_name:
 - NetLocalGroupGetMembers
---

# NetLocalGroupGetMembers function


## -description

The 
				<b>NetLocalGroupGetMembers</b> function retrieves a list of the members of a particular local group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory. Local group members can be users or global groups.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param localgroupname [in]

Pointer to a constant string that specifies the name of the local group whose members are to be listed. For more information, see the following Remarks section.

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
Return the 
<a href="/windows/desktop/SecAuthZ/security-identifiers">security identifier</a> (SID) associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the SID and account information associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_1">LOCALGROUP_MEMBERS_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return the SID, account information, and the domain name associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_2">LOCALGROUP_MEMBERS_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return the account and domain names of the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the address that receives the return information structure. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position.

### -param resumehandle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing group member search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, then no resume handle is stored.

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
<dt><b>ERROR_NO_SUCH_ALIAS</b></dt>
</dl>
</td>
<td width="60%">
The specified local group does not exist.

</td>
</tr>
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function. 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

If this function returns <b>ERROR_MORE_DATA</b>, then it must be repeatedly called until <b>ERROR_SUCCESS</b> or <b>NERR_success</b> is returned.  Failure to do so can result in an RPC connection leak.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_1">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_2">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group
		  Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupenum">NetLocalGroupEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetinfo">NetLocalGroupGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetmembers">NetLocalGroupSetMembers</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>