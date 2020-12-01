---
UID: NF:mprapi.MprConfigServerGetInfoEx
title: MprConfigServerGetInfoEx function (mprapi.h)
description: The MprConfigServerGetInfoEx function retrieves port information for a specified server.
helpviewer_keywords: ["MprConfigServerGetInfoEx","MprConfigServerGetInfoEx function [RAS]","mprapi/MprConfigServerGetInfoEx","rras.mprconfigservergetinfoex"]
old-location: rras\mprconfigservergetinfoex.htm
tech.root: RRAS
ms.assetid: 654d1410-b54c-4284-bf7f-f6ae6b7ef85e
ms.date: 12/05/2018
ms.keywords: MprConfigServerGetInfoEx, MprConfigServerGetInfoEx function [RAS], mprapi/MprConfigServerGetInfoEx, rras.mprconfigservergetinfoex
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
 - MprConfigServerGetInfoEx
 - mprapi/MprConfigServerGetInfoEx
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
 - MprConfigServerGetInfoEx
---

# MprConfigServerGetInfoEx function


## -description

The 
<b>MprConfigServerGetInfoEx</b> function retrieves port information for a specified server.

## -parameters

### -param hMprConfig [in]

A handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param pServerInfo [out]

A pointer, on output, to  a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_ex0">MPR_SERVER_EX</a> structure that contains the port information for the RRAS server in <i>hMprConfig</i>.

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
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfoex">MprAdminServerGetInfoEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfoex">MprAdminServerSetInfoEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>