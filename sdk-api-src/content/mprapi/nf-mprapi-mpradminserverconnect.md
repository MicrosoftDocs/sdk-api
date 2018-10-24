---
UID: NF:mprapi.MprAdminServerConnect
title: MprAdminServerConnect function
author: windows-sdk-content
description: The MprAdminServerConnect function establishes a connection to a router for the purpose of administering that router.
old-location: rras\mpradminserverconnect.htm
tech.root: rras
ms.assetid: f93b37bc-d3d1-40f0-aef6-839bb43c88e2
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: MprAdminServerConnect, MprAdminServerConnect function [RAS], _mpr_mpradminserverconnect, mprapi/MprAdminServerConnect, rras.mpradminserverconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminServerConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

