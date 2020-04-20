---
UID: NF:lmaccess.NetGroupGetInfo
title: NetGroupGetInfo function (lmaccess.h)
description: The NetGroupGetInfo function retrieves information about a particular global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.helpviewer_keywords: ["0","1","2","3","NetGroupGetInfo","NetGroupGetInfo function [Network Management]","_win32_netgroupgetinfo","lmaccess/NetGroupGetInfo","netmgmt.netgroupgetinfo"]
old-location: netmgmt\netgroupgetinfo.htm
tech.root: NetMgmt
ms.assetid: f9957c15-9a49-4b53-ae31-efd6a03417a6
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, NetGroupGetInfo, NetGroupGetInfo function [Network Management], _win32_netgroupgetinfo, lmaccess/NetGroupGetInfo, netmgmt.netgroupgetinfo
f1_keywords:
- lmaccess/NetGroupGetInfo
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
- NetGroupGetInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetGroupGetInfo function


## -description


The
				<b>NetGroupGetInfo</b> function retrieves information about a particular global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -parameters




### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param groupname [in]

Pointer to a constant string that specifies the name of the global group for which to retrieve information. For more information, see the following Remarks section.


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
Return the global group name. The <i>bufptr</i> parameter points to a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the global group name and a comment. The <i>bufptr</i> parameter points to a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about the global group. The <i>bufptr</i> parameter points to a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_2">GROUP_INFO_2</a> structure. Note that on Windows XP and later, it is recommended that you use 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Return detailed information about the global group. The <i>bufptr</i> parameter points to a 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> structure.

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the address of the buffer that receives the global group information structure. The format of this data depends on the value of the <i>level</i> parameter. The system allocates the memory for this buffer. You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function to deallocate the memory. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.


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
<dt><b>NERR_GroupNotFound</b></dt>
</dl>
</td>
<td width="60%">
The global group name could not be found.

</td>
</tr>
</table>
 




## -remarks



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The security descriptor of the Group object is used to perform the access check for this function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_0">GROUP_INFO_0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_1">GROUP_INFO_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>
 

 

