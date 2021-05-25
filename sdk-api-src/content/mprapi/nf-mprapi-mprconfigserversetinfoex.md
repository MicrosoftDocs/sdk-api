---
UID: NF:mprapi.MprConfigServerSetInfoEx
title: MprConfigServerSetInfoEx function (mprapi.h)
description: The MprConfigServerSetInfoEx function sets port information on a specified RRAS server.
helpviewer_keywords: ["MprConfigServerSetInfoEx","MprConfigServerSetInfoEx function [RAS]","mprapi/MprConfigServerSetInfoEx","rras.mprconfigserversetinfoex"]
old-location: rras\mprconfigserversetinfoex.htm
tech.root: RRAS
ms.assetid: 8251f391-7697-4024-9a9d-c7c810129a78
ms.date: 12/05/2018
ms.keywords: MprConfigServerSetInfoEx, MprConfigServerSetInfoEx function [RAS], mprapi/MprConfigServerSetInfoEx, rras.mprconfigserversetinfoex
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
 - MprConfigServerSetInfoEx
 - mprapi/MprConfigServerSetInfoEx
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
 - MprConfigServerSetInfoEx
---

# MprConfigServerSetInfoEx function


## -description

The 
<b>MprConfigServerSetInfoEx</b> function sets port information on a specified  RRAS server.

## -parameters

### -param hMprConfig [in]

A handle to the router configuration. Obtain this handle by calling <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param pSetServerConfig [in]

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -remarks

These changes to a server configuration are persistent, but have no effect on a RRAS server until it is restarted.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfo">MprConfigServerGetInfo</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>