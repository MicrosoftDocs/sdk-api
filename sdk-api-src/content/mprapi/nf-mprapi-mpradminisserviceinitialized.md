---
UID: NF:mprapi.MprAdminIsServiceInitialized
title: MprAdminIsServiceInitialized function (mprapi.h)
description: The MprAdminIsServiceInitialized function checks whether the RRAS service is running on a specified server if the calling process has access.
helpviewer_keywords: ["FALSE","MprAdminIsServiceInitialized","MprAdminIsServiceInitialized function [RAS]","TRUE","mprapi/MprAdminIsServiceInitialized","rras.mpradminisserviceinitialized"]
old-location: rras\mpradminisserviceinitialized.htm
tech.root: RRAS
ms.assetid: 912bbb7d-f566-4297-b412-605658acaac8
ms.date: 12/05/2018
ms.keywords: FALSE, MprAdminIsServiceInitialized, MprAdminIsServiceInitialized function [RAS], TRUE, mprapi/MprAdminIsServiceInitialized, rras.mpradminisserviceinitialized
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminIsServiceInitialized
 - mprapi/MprAdminIsServiceInitialized
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
 - MprAdminIsServiceInitialized
---

# MprAdminIsServiceInitialized function


## -description

The 
<b>MprAdminIsServiceInitialized</b> function checks whether the RRAS service is running on a specified server if the calling process has access.

## -parameters

### -param lpwsServerName [in]

A pointer to a <b>null</b>-terminated Unicode string that specifies the name of the server to query. If this parameter is <b>NULL</b>, the function queries the local machine.

### -param fIsServiceInitialized [in]

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

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminisservicerunning">MprAdminIsServiceRunning</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>