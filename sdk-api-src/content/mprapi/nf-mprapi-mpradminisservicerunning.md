---
UID: NF:mprapi.MprAdminIsServiceRunning
title: MprAdminIsServiceRunning function (mprapi.h)
description: The MprAdminIsServiceRunning function checks whether the RRAS service is running on a specified server if the calling process has access.
helpviewer_keywords: ["MprAdminIsServiceRunning","MprAdminIsServiceRunning function [RAS]","_mpr_mpradminisservicerunning","mprapi/MprAdminIsServiceRunning","rras.mpradminisservicerunning"]
old-location: rras\mpradminisservicerunning.htm
tech.root: RRAS
ms.assetid: 3722e5f2-3cd7-490a-84b7-4a1c9fa11de7
ms.date: 12/05/2018
ms.keywords: MprAdminIsServiceRunning, MprAdminIsServiceRunning function [RAS], _mpr_mpradminisservicerunning, mprapi/MprAdminIsServiceRunning, rras.mpradminisservicerunning
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminIsServiceRunning
 - mprapi/MprAdminIsServiceRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminIsServiceRunning
---

# MprAdminIsServiceRunning function


## -description

The 
<b>MprAdminIsServiceRunning</b> function checks whether the RRAS service is running on a specified server  if the calling process has access.

## -parameters

### -param lpwsServerName [in]

A pointer to a <b>null</b>-terminated Unicode string that specifies the name of the server to query. If this parameter is <b>NULL</b>, the function queries the local machine.

## -returns

The return value is one of the following Boolean values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The service is running on the specified server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The service is not running on the specified server and/or the calling process does not have access to the RRAS service.

</td>
</tr>
</table>

## -remarks

This function returns <b>FALSE</b> if the RRAS service is running, but the calling process does not have  sufficient privileges to access the service. If the access rights of the calling process on the server are unknown, it is recommended that <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a> is called prior to calling this function. Doing so will determine  if the process has the required access rights to the server.

## -see-also

<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>