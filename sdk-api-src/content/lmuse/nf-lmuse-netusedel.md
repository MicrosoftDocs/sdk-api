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

# NetUseDel function


## -description


The
				<b>NetUseDel</b> function ends a connection to a shared resource.

You can also use the 
<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a> function to terminate a network connection.


## -parameters




### -param OPTIONAL

TBD


### -param UseName [in]

A pointer to a string that specifies the path of the connection to delete.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -param ForceLevelFlags

TBD




#### - ForceCond [in]

The level of force to use in deleting the connection.

 This parameter can be one of the following values defined in the <i>lmuseflg.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USE_NOFORCE"></a><a id="use_noforce"></a><dl>
<dt><b>USE_NOFORCE</b></dt>
</dl>
</td>
<td width="60%">
Fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_FORCE"></a><a id="use_force"></a><dl>
<dt><b>USE_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Do not fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_LOTS_OF_FORCE"></a><a id="use_lots_of_force"></a><dl>
<dt><b>USE_LOTS_OF_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Close any open files and delete the connection.

</td>
</tr>
</table>
 


#### - UncServerName [in]

The UNC name of the computer on which to execute this function. If this is parameter is <b>NULL</b>, then the local computer is used. 

If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism. 

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The <b>NetUseDel</b> function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseDel</b> function does not support Distributed File System (DFS) shares or other network file systems. To terminate a connection to a share using a different network provider (WebDAV or a DFS share, for example), use the <a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a> function.


No special group membership is required to call the 
<b>NetUseDel</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility.




## -see-also




<a href="https://msdn.microsoft.com/22550c17-003a-4f59-80f0-58fa3e286844">NetUseAdd</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>



<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a>
 

 

