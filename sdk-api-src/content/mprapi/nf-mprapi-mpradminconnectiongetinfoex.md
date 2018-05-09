---
UID: NF:mprapi.MprAdminConnectionGetInfoEx
title: MprAdminConnectionGetInfoEx function
author: windows-driver-content
description: Retrieves the connection information for a specific connection on a specified RRAS server.
old-location: rras\mpradminconnectiongetinfoex.htm
old-project: RRAS
ms.assetid: 7b6a27da-306c-48e5-830b-215ce6f80ea1
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: MprAdminConnectionGetInfoEx, MprAdminConnectionGetInfoEx function [RAS], mprapi/MprAdminConnectionGetInfoEx, rras.mpradminconnectiongetinfoex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
-	MprAdminConnectionGetInfoEx
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminConnectionGetInfoEx function


## -description


The 
<b>MprAdminConnectionGetInfoEx</b> function retrieves the connection information for a specific connection on a specified RRAS server.


## -parameters




### -param hRasServer [in]

A handle to the computer from which the connection information is retrieved. To obtain this handle, call <a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hRasConnection

TBD


### -param pRasConnection [out]

A pointer, on output, to  a <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure that contains the connection information for the RRAS server in <i>hRasServer</i>.

To free this memory, call <a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


#### - hConnection [in]

A handle to the connection to retrieve data about. To obtain this handle, call <a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>.


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
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>
 




## -remarks



The caller should free the memory pointed to by <i>pRasConnection</i> by calling the function <a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/1fef5fbf-de3f-43c6-8b94-808f6ed209d8">MprAdminConnectionGetInfo</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

