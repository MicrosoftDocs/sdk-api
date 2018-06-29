---
UID: NF:mprapi.MprConfigServerConnect
title: MprConfigServerConnect function
author: windows-sdk-content
description: The MprConfigServerConnect function connects to the router to be configured.
old-location: rras\mprconfigserverconnect.htm
old-project: RRAS
ms.assetid: 40029088-191d-49b1-88d3-79ffb2da0eef
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprConfigServerConnect, MprConfigServerConnect function [RAS], _mpr_mprconfigserverconnect, mprapi/MprConfigServerConnect, rras.mprconfigserverconnect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigServerConnect
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigServerConnect function


## -description


The 
<b>MprConfigServerConnect</b> function connects to the router to be configured. Call this function before making any other calls to the server. The handle returned by this function is used in subsequent calls to configure interfaces and transports on the server.


## -parameters




### -param lpwsServerName [in]

Pointer to a Unicode string that specifies the name of the remote server to configure. If this parameter is <b>NULL</b>, the function returns a handle to the router configuration on the local machine.


### -param phMprConfig [out]

Pointer to a handle variable. This variable receives a handle to the router configuration.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>phMprConfig</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

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
<a href="https://msdn.microsoft.com/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/71cdb26b-e9d0-414c-aff9-0eed187d08ba">MprConfigServerDisconnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

