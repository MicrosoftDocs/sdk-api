---
UID: NF:mprapi.MprConfigServerSetInfo
title: MprConfigServerSetInfo function
author: windows-driver-content
description: The MprAdminIsServiceInitialized function checks whether the RRAS service is running on a specified server if the calling process has access.
old-location: rras\mpradminisserviceinitialized.htm
old-project: RRAS
ms.assetid: 912bbb7d-f566-4297-b412-605658acaac8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FALSE, MprConfigServerSetInfo, MprConfigServerSetInfo function [RAS], TRUE, mprapi/MprConfigServerSetInfo, rras.mpradminisserviceinitialized
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
-	MprConfigServerSetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigServerSetInfo function


## -description


The 
<b>MprAdminIsServiceInitialized</b> function checks whether the RRAS service is running on a specified server if the calling process has access. 


## -parameters




### -param hMprServer

TBD


### -param dwLevel

TBD


### -param lpbBuffer

TBD




#### - fIsServiceInitialized [in]

On output, a pointer to a BOOL   that specifies whether the RRAS service is running on the server in <i>lpwsServerName</i>:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The service is running on the specified server.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The service is not running on the specified server and/or the calling process does not have access to the RRAS service.

</td>
</tr>
</table>
 


#### - lpwsServerName [in]

A pointer to a <b>null</b>-terminated Unicode string that specifies the name of the server to query. If this parameter is <b>NULL</b>, the function queries the local machine.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>fIsServiceInitialized</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The RRAS service is not running on the server.

</td>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3722e5f2-3cd7-490a-84b7-4a1c9fa11de7">MprAdminIsServiceRunning</a>



<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

