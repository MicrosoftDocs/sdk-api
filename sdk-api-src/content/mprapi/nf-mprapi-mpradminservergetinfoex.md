---
UID: NF:mprapi.MprAdminServerGetInfoEx
title: MprAdminServerGetInfoEx function (mprapi.h)
description: The MprAdminServerGetInfoEx function retrieves port information about the specified RRAS server.
helpviewer_keywords: ["MprAdminServerGetInfoEx","MprAdminServerGetInfoEx function [RAS]","mprapi/MprAdminServerGetInfoEx","rras.mpradminservergetinfoex"]
old-location: rras\mpradminservergetinfoex.htm
tech.root: RRAS
ms.assetid: 19fff58d-6e13-478f-a960-de5d0702661c
ms.date: 12/05/2018
ms.keywords: MprAdminServerGetInfoEx, MprAdminServerGetInfoEx function [RAS], mprapi/MprAdminServerGetInfoEx, rras.mpradminservergetinfoex
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
 - MprAdminServerGetInfoEx
 - mprapi/MprAdminServerGetInfoEx
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
 - MprAdminServerGetInfoEx
---

# MprAdminServerGetInfoEx function


## -description

The 
<b>MprAdminServerGetInfoEx</b> function retrieves port information about the specified RRAS server.

## -parameters

### -param hMprServer [in]

A handle to the server to query. Obtain this handle by calling <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param pServerInfo [out]

A pointer, on output, to  a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_ex0">MPR_SERVER_EX</a> structure that contains the port information for the RRAS server in <i>hMprServer</i>.

To free this memory, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfoex">MprAdminServerSetInfoEx</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>