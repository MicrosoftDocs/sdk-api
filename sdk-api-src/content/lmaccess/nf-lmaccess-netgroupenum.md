---
UID: NF:lmaccess.NetGroupEnum
title: NetGroupEnum function
author: windows-sdk-content
description: The NetGroupEnum function retrieves information about each global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\netgroupenum.htm
tech.root: netmgmt
ms.assetid: 3f8fabce-94cb-41f5-9af1-04585ac3f16e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: 0, 1, 2, 3, NetGroupEnum, NetGroupEnum function [Network Management], _win32_netgroupenum, lmaccess/NetGroupEnum, netmgmt.netgroupenum
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - NetGroupEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetGroupEnum function


## -description


The
				<b>NetGroupEnum</b> function retrieves information about each global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

The 
<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a> function provides an efficient mechanism for enumerating global groups. When possible, it is recommended that you use 
<b>NetQueryDisplayInformation</b> instead of the 
<b>NetGroupEnum</b> function.


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
Return the global group name. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/019796d1-b987-45d2-90df-1d3b484217a9">GROUP_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the global group name and a comment. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/0b42a438-64fd-4f37-98b8-77e10c09548c">GROUP_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return detailed information about the global group. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/2c17a70c-7b62-4dcc-9dc6-2f4b8c41d6ec">GROUP_INFO_2</a> structures. Note that on Windows XP and later, it is recommended that you use 
<a href="https://msdn.microsoft.com/aa0c3b6e-ab27-48b9-a37f-5cceb63c70fd">GROUP_INFO_3</a> instead.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Return detailed information about the global group. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/aa0c3b6e-ab27-48b9-a37f-5cceb63c70fd">GROUP_INFO_3</a> structures.

<b>Windows 2000:  </b>This level is not supported.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer to receive the global group information structure. The format of this data depends on the value of the <i>level</i> parameter. 




The system allocates the memory for this buffer. You must call the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function to deallocate the memory. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.


### -param prefmaxlen [in]

Specifies the preferred maximum length of the returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required to hold the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. The total number of entries is only a hint. For more information about determining the exact number of entries, see the following Remarks section.


### -param resume_handle [in, out]

Pointer to a variable that contains a resume handle that is used to continue the global group enumeration. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, no resume handle is stored.


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
</table>
 




## -remarks



If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management group functions. For more information, see 
<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>.

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="security.pre_windows_2000_compatible_access_group">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The function only returns information to which the caller has Read access. The caller must have List Contents access to the Domain object, and  Enumerate Entire SAM Domain access on the SAM Server object  located in the System container. 

To determine the exact total number of groups, you must enumerate the entire tree, which can be a costly operation. To enumerate the entire tree, use the <i>resume_handle</i> parameter to continue the enumeration for consecutive calls, and use the <i>entriesread</i> parameter to accumulate the total number of groups. If your application is communicating with a domain controller, you should consider using the 
<a href="https://msdn.microsoft.com/3c13ea2f-fe40-4fd4-8540-422f277e07c1">ADSI LDAP Provider</a> to retrieve this type of data more efficiently. The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces. For more information, see 
<a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI Service Providers</a>.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/019796d1-b987-45d2-90df-1d3b484217a9">GROUP_INFO_0</a>



<a href="https://msdn.microsoft.com/0b42a438-64fd-4f37-98b8-77e10c09548c">GROUP_INFO_1</a>



<a href="https://msdn.microsoft.com/aa0c3b6e-ab27-48b9-a37f-5cceb63c70fd">GROUP_INFO_3</a>



<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>



<a href="https://msdn.microsoft.com/f9957c15-9a49-4b53-ae31-efd6a03417a6">NetGroupGetInfo</a>



<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a>



<a href="https://msdn.microsoft.com/049f1ea3-4d23-4b35-8b08-7256859aed45">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

