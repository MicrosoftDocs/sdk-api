---
UID: NF:lmaccess.NetLocalGroupGetMembers
title: NetLocalGroupGetMembers function
author: windows-sdk-content
description: The NetLocalGroupGetMembers function retrieves a list of the members of a particular local group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\netlocalgroupgetmembers.htm
old-project: netmgmt
ms.assetid: 35770b32-dae9-46f5-84e3-1c31ca22f708
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0, 1, 2, 3, NetLocalGroupGetMembers, NetLocalGroupGetMembers function [Network Management], _win32_netlocalgroupgetmembers, lmaccess/NetLocalGroupGetMembers, netmgmt.netlocalgroupgetmembers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetLocalGroupGetMembers
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="security.security_identifiers_sids_">security identifier</a> (SID) associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the SID and account information associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return the SID, account information, and the domain name associated with the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/f5cd6e84-1111-4558-bec4-26af13f21b61">LOCALGROUP_MEMBERS_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return the account and domain names of the local group member. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the address that receives the return information structure. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.


### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


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



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="security.pre_windows_2000_compatible_access_group">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the LocalGroup object is used to perform the access check for this function. 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management local group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.

If this function returns <b>ERROR_MORE_DATA</b>, then it must be repeatedly called until <b>ERROR_SUCCESS</b> or <b>NERR_success</b> is returned.  Failure to do so can result in an RPC connection leak.




## -see-also




<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://msdn.microsoft.com/f5cd6e84-1111-4558-bec4-26af13f21b61">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group
		  Functions</a>



<a href="https://msdn.microsoft.com/fc27d7f1-bfbe-46d7-a154-f04eb9249248">NetLocalGroupEnum</a>



<a href="https://msdn.microsoft.com/ee2f0be9-8d52-439b-ab65-f9e11a2872c5">NetLocalGroupGetInfo</a>



<a href="https://msdn.microsoft.com/4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c">NetLocalGroupSetMembers</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

