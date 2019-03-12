---
UID: NF:lmaccess.NetLocalGroupGetInfo
title: NetLocalGroupGetInfo function
author: windows-sdk-content
description: The NetLocalGroupGetInfo function retrieves information about a particular local group account on a server.
old-location: netmgmt\netlocalgroupgetinfo.htm
tech.root: NetMgmt
ms.assetid: ee2f0be9-8d52-439b-ab65-f9e11a2872c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 1, NetLocalGroupGetInfo, NetLocalGroupGetInfo function [Network Management], _win32_netlocalgroupgetinfo, lmaccess/NetLocalGroupGetInfo, netmgmt.netlocalgroupgetinfo
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
 - NetLocalGroupGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetLocalGroupGetInfo function


## -description


The 
				<b>NetLocalGroupGetInfo</b> function retrieves information about a particular local group account on a server.


## -parameters




### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param groupname [in]

Pointer to a constant string that specifies the name of the local group account for which the information will be retrieved. For more information, see the following Remarks section.


### -param level [in]

Specifies the information level of the data. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the comment associated with the local group. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the address of the buffer that receives the return information structure. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


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
The specified local group does not exist.

</td>
</tr>
</table>
 




## -remarks



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="https://msdn.microsoft.com/library/Aa375347(v=VS.85).aspx">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.




## -see-also




<a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group
		  Functions</a>



<a href="https://msdn.microsoft.com/fc27d7f1-bfbe-46d7-a154-f04eb9249248">NetLocalGroupEnum</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a>



<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

