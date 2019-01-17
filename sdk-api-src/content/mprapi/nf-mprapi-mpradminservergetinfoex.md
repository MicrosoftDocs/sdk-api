---
UID: NF:mprapi.MprAdminServerGetInfoEx
title: MprAdminServerGetInfoEx function
author: windows-sdk-content
description: The MprAdminServerGetInfoEx function retrieves port information about the specified RRAS server.
old-location: rras\mpradminservergetinfoex.htm
tech.root: RRAS
ms.assetid: 19fff58d-6e13-478f-a960-de5d0702661c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprAdminServerGetInfoEx, MprAdminServerGetInfoEx function [RAS], mprapi/MprAdminServerGetInfoEx, rras.mpradminservergetinfoex
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MprAdminServerGetInfoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminServerGetInfoEx function


## -description


The 
<b>MprAdminServerGetInfoEx</b> function retrieves port information about the specified RRAS server.


## -parameters




### -param hMprServer [in]

A handle to the server to query. Obtain this handle by calling <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param pServerInfo [out]

A pointer, on output, to  a <a href="https://msdn.microsoft.com/10c1e3bd-adb8-4aff-835c-e7d881c9f5cf">MPR_SERVER_EX</a> structure that contains the port information for the RRAS server in <i>hMprServer</i>.

To free this memory, call <a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

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
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PROC_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified procedure could not be found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/6109d6e0-21ce-4837-9e94-83318c9af3d8">MprAdminServerSetInfoEx</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

