---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NetUseGetInfo function


## -description


The
				<b>NetUseGetInfo</b> function retrieves information about a connection to a shared resource.

You can also use the 
<a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a> function to retrieve the name of a network resource associated with a local device.


## -parameters




### -param UncServerName [in]

The UNC name of computer on which to execute this function. If this is parameter is <b>NULL</b>, then the local computer is used. If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism. 

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -param UseName [in]

A pointer to a string that specifies the name of the connection for which to return information.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -param LevelFlags

TBD


### -param bufptr

TBD




#### - BufPtr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


#### - Level [in]

The information level of the data requested. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Specifies a local device name and the share name of a remote resource. The <i>BufPtr</i>  parameter is a pointer to a 
<a href="https://msdn.microsoft.com/86db3f19-84c5-4e89-82cb-f01d17dcf4ec">USE_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource, including connection status and type. The <i>BufPtr</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource. Information includes the connection status, connection type, user name, and domain name. The <i>BufPtr</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a> structure.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required to call the 
<b>NetUseGetInfo</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility.

To list all current connections between the local computer and resources on remote servers, you can call the 
<a href="https://msdn.microsoft.com/fb527f85-baea-48e8-b837-967870834ec5">NetUseEnum</a> function.

This function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseGetInfo</b> function does not support Distributed File System (DFS) shares. To retrieve information for a share using a different network provider (WebDAV or a DFS share, for example), use the <a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a> function.






## -see-also




<a href="https://msdn.microsoft.com/fb527f85-baea-48e8-b837-967870834ec5">NetUseEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/86db3f19-84c5-4e89-82cb-f01d17dcf4ec">USE_INFO_0</a>



<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a>



<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>



<a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a>
 

 

