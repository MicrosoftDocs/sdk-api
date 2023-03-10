---
UID: NF:mprapi.MprConfigServerConnect
title: MprConfigServerConnect function (mprapi.h)
description: The MprConfigServerConnect function connects to the router to be configured.
helpviewer_keywords: ["MprConfigServerConnect","MprConfigServerConnect function [RAS]","_mpr_mprconfigserverconnect","mprapi/MprConfigServerConnect","rras.mprconfigserverconnect"]
old-location: rras\mprconfigserverconnect.htm
tech.root: RRAS
ms.assetid: 40029088-191d-49b1-88d3-79ffb2da0eef
ms.date: 12/05/2018
ms.keywords: MprConfigServerConnect, MprConfigServerConnect function [RAS], _mpr_mprconfigserverconnect, mprapi/MprConfigServerConnect, rras.mprconfigserverconnect
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
 - MprConfigServerConnect
 - mprapi/MprConfigServerConnect
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
 - MprConfigServerConnect
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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverdisconnect">MprConfigServerDisconnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>