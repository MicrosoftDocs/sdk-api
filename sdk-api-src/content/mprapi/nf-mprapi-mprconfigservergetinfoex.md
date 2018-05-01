---
UID: NF:mprapi.MprConfigServerGetInfoEx
title: MprConfigServerGetInfoEx function
author: windows-driver-content
description: The MprConfigServerGetInfoEx function retrieves port information for a specified server.
old-location: rras\mprconfigservergetinfoex.htm
old-project: RRAS
ms.assetid: 654d1410-b54c-4284-bf7f-f6ae6b7ef85e
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MprConfigServerGetInfoEx, MprConfigServerGetInfoEx function [RAS], mprapi/MprConfigServerGetInfoEx, rras.mprconfigservergetinfoex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprConfigServerGetInfoEx
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigServerGetInfoEx function


## -description


The 
<b>MprConfigServerGetInfoEx</b> function retrieves port information for a specified server.


## -parameters




### -param hMprConfig [in]

A handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param pServerInfo [out]

A pointer, on output, to  a <a href="https://msdn.microsoft.com/10c1e3bd-adb8-4aff-835c-e7d881c9f5cf">MPR_SERVER_EX</a> structure that contains the port information for the RRAS server in <i>hMprConfig</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/19fff58d-6e13-478f-a960-de5d0702661c">MprAdminServerGetInfoEx</a>



<a href="https://msdn.microsoft.com/6109d6e0-21ce-4837-9e94-83318c9af3d8">MprAdminServerSetInfoEx</a>



<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

