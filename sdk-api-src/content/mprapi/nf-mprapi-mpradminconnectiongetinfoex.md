---
UID: NF:mprapi.MprAdminConnectionGetInfoEx
title: MprAdminConnectionGetInfoEx function (mprapi.h)
description: Retrieves the connection information for a specific connection on a specified RRAS server.
helpviewer_keywords: ["MprAdminConnectionGetInfoEx","MprAdminConnectionGetInfoEx function [RAS]","mprapi/MprAdminConnectionGetInfoEx","rras.mpradminconnectiongetinfoex"]
old-location: rras\mpradminconnectiongetinfoex.htm
tech.root: RRAS
ms.assetid: 7b6a27da-306c-48e5-830b-215ce6f80ea1
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionGetInfoEx, MprAdminConnectionGetInfoEx function [RAS], mprapi/MprAdminConnectionGetInfoEx, rras.mpradminconnectiongetinfoex
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminConnectionGetInfoEx
 - mprapi/MprAdminConnectionGetInfoEx
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
 - MprAdminConnectionGetInfoEx
---

# MprAdminConnectionGetInfoEx function


## -description

The 
<b>MprAdminConnectionGetInfoEx</b> function retrieves the connection information for a specific connection on a specified RRAS server.

## -parameters

### -param hRasServer [in]

A handle to the computer from which the connection information is retrieved. To obtain this handle, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hRasConnection [in]

A handle to the connection to retrieve data about. To obtain this handle, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>.

### -param pRasConnection [out]

A pointer, on output, to  a <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure that contains the connection information for the RRAS server in <i>hRasServer</i>.

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

The caller should free the memory pointed to by <i>pRasConnection</i> by calling the function <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectiongetinfo">MprAdminConnectionGetInfo</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>