---
UID: NF:lmaccess.NetLocalGroupAdd
title: NetLocalGroupAdd function
author: windows-sdk-content
description: The NetLocalGroupAdd function creates a local group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\netlocalgroupadd.htm
old-project: netmgmt
ms.assetid: 5028c1bc-8fed-4f02-8e69-d0d122b08d9f
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: 0, 1, NetLocalGroupAdd, NetLocalGroupAdd function [Network Management], _win32_netlocalgroupadd, lmaccess/NetLocalGroupAdd, netmgmt.netlocalgroupadd
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - Samcli.dll
api_name:
 - NetLocalGroupAdd
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetLocalGroupAdd function


## -description


The
				<b>NetLocalGroupAdd</b> function creates a local group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -parameters




### -param OPTIONAL

TBD




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
A local group name. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/dfdb4c20-ea4a-45c9-b4f3-d6a844f89bb6">LOCALGROUP_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
A local group name and a comment to associate with the group. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a> structure.

</td>
</tr>
</table>
 


### -param buf [in]

A pointer to a buffer that contains the local group information structure. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


#### - parm_err [out]

A pointer to a value that receives the index of the first member of the local group information structure to cause the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the Remarks section in the 
<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a> topic.


#### - servername [in]

A pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


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
The caller does not have the appropriate
        access to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALIAS_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified local group already exists. This error is returned if the group name member in the structure pointed to by the <i>buf</i> parameter is already in use as an alias.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
A <i>level</i> parameter is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if one or more of the members in the structure pointed to by the <i>buf</i> parameter is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_GroupExists</b></dt>
</dl>
</td>
<td width="60%">
The group name exists. This error is returned if the group name member in the structure pointed to by the <i>buf</i> parameter is already in use as a group name.

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
<dt><b>NERR_UserExists</b></dt>
</dl>
</td>
<td width="60%">
The user name exists. This error is returned if the group name member in the structure pointed to by the <i>buf</i> parameter is already in use as a user name.

</td>
</tr>
</table>
 




## -remarks



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Power Users can call this function. For more information, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The security descriptor of the user container is used to perform the access check for this function. The caller must be able to create child objects of the group class.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

If the 
<b>NetLocalGroupAdd</b> function returns <b>ERROR_INVALID_PARAMETER</b> and a <b>NULL</b> pointer was not passed in <i>parm_err</i> parameter, on return the <i>parm_err</i> parameter indicates the first member of the local group information structure that is invalid. The format of the local group information structure is specified in the <i>level</i> parameter. A pointer to the local group information structure is passed in <i>buf</i> parameter. The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. 

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>LOCALGROUP_NAME_PARMNUM</td>
<td>
If the <i>level</i> parameter was 0, the <b>lgrpi0_name</b> member of the <a href="https://msdn.microsoft.com/dfdb4c20-ea4a-45c9-b4f3-d6a844f89bb6">LOCALGROUP_INFO_0</a> 
		 structure was invalid.

If the <i>level</i> parameter was 1, the <b>lgrpi1_name</b> member of the <a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a> 
		 structure was invalid.  

</td>
</tr>
<tr>
<td>LOCALGROUP_COMMENT_PARMNUM</td>
<td>
If the <i>level</i> parameter was 1, the <b>lgrpi1_comment</b> member of the <a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a> 
		 structure was invalid.  

</td>
</tr>
</table>
 

When making requests to a domain controller and Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same results as the network management local group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.




## -see-also




<a href="https://msdn.microsoft.com/dfdb4c20-ea4a-45c9-b4f3-d6a844f89bb6">LOCALGROUP_INFO_0</a>



<a href="https://msdn.microsoft.com/b96d7ddc-3ffb-4203-88b1-4aa123051695">LOCALGROUP_INFO_1</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group
		  Functions</a>



<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a>



<a href="https://msdn.microsoft.com/b26bfd52-c20a-4f6f-9503-87cac5168362">NetLocalGroupDel</a>



<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>
 

 

