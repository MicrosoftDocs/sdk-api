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

# MprAdminServerConnect function


## -description


The 
<b>MprAdminServerConnect</b> function establishes a connection to a router for the purpose of administering that router. Call this function before making any other calls to the server. Use the handle returned in subsequent calls to administer interfaces on the server.


## -parameters




### -param lpwsServerName [in, optional]

A pointer to a <b>null</b>-terminated Unicode string that specifies the name of the remote server. If this parameter is <b>NULL</b>, the function returns a handle to the local machine.


### -param phMprServer [out]

A pointer to a <b>HANDLE</b> variable that receives a handle to the server. Use this handle in subsequent calls to administer the server.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privilege.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This function was called with <i>phMprServer</i> parameter equal to  <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_IF</b></dt>
</dl>
</td>
<td width="60%">
The specified computer is not running the Routing and RAS service.

</td>
</tr>
</table>
 




## -remarks



<b>MprAdminIsServiceRunning</b> must be used to determine the status of the RRAS service on the remote server. <b>MprAdminServerConnect</b> does not query the RRAS service when establishing a connection.




## -see-also




<a href="https://msdn.microsoft.com/905b5296-ae6b-40a6-ba49-837db96de152">MprAdminServerDisconnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

