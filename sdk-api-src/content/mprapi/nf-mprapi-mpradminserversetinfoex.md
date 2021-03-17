---
UID: NF:mprapi.MprAdminServerSetInfoEx
title: MprAdminServerSetInfoEx function (mprapi.h)
description: The MprAdminServerSetInfoEx function sets port information on a specified RRAS server.
helpviewer_keywords: ["MprAdminServerSetInfoEx","MprAdminServerSetInfoEx function [RAS]","mprapi/MprAdminServerSetInfoEx","rras.mpradminserversetinfoex"]
old-location: rras\mpradminserversetinfoex.htm
tech.root: RRAS
ms.assetid: 6109d6e0-21ce-4837-9e94-83318c9af3d8
ms.date: 12/05/2018
ms.keywords: MprAdminServerSetInfoEx, MprAdminServerSetInfoEx function [RAS], mprapi/MprAdminServerSetInfoEx, rras.mpradminserversetinfoex
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
 - MprAdminServerSetInfoEx
 - mprapi/MprAdminServerSetInfoEx
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
 - MprAdminServerSetInfoEx
---

# MprAdminServerSetInfoEx function


## -description

The 
<b>MprAdminServerSetInfoEx</b> function sets port information on a specified  RRAS server.

## -parameters

### -param hMprServer [in]

A handle to the router to query. Obtain this handle by calling <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param pServerInfo [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_set_config_ex0">MPR_SERVER_SET_CONFIG_EX</a> structure that contains the port information being set on the server in <i>hMprServer</i>.

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

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfoex">MprAdminServerGetInfoEx</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>