---
UID: NF:mprapi.MprConfigServerSetInfoEx
title: MprConfigServerSetInfoEx function (mprapi.h)
author: windows-sdk-content
description: The MprConfigServerSetInfoEx function sets port information on a specified RRAS server.
old-location: rras\mprconfigserversetinfoex.htm
tech.root: RRAS
ms.assetid: 8251f391-7697-4024-9a9d-c7c810129a78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprConfigServerSetInfoEx, MprConfigServerSetInfoEx function [RAS], mprapi/MprConfigServerSetInfoEx, rras.mprconfigserversetinfoex
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
 - MprConfigServerSetInfoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigServerSetInfoEx function


## -description


The 
<b>MprConfigServerSetInfoEx</b> function sets port information on a specified  RRAS server.


## -parameters




### -param hMprConfig [in]

A handle to the router configuration. Obtain this handle by calling <a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>. 


### -param pSetServerConfig [in]

A pointer to a 
<a href="https://msdn.microsoft.com/6c993c9c-4522-4758-926a-fa7ef2a89418">MPR_SERVER_SET_CONFIG_EX</a> structure that contains the port information being set on the server in <i>hMprServer</i>.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>pSetServerConfig</b> parameter is <b>NULL</b> or the <b>Header</b> field values are erroneous.

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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



These changes to a server configuration are persistent, but have no affect on a RRAS server until it is restarted.




## -see-also




<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b">MprConfigServerGetInfo</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

