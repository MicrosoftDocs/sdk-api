---
UID: NF:mprapi.MprConfigTransportGetHandle
title: MprConfigTransportGetHandle function (mprapi.h)
description: The MprConfigTransportGetHandle function retrieves a handle to the specified transport protocol's configuration in the specified router configuration.
helpviewer_keywords: ["MprConfigTransportGetHandle","MprConfigTransportGetHandle function [RAS]","_mpr_mprconfigtransportgethandle","mprapi/MprConfigTransportGetHandle","rras.mprconfigtransportgethandle"]
old-location: rras\mprconfigtransportgethandle.htm
tech.root: RRAS
ms.assetid: 2d3a2300-de10-4ee0-ba0e-bda26cf9a910
ms.date: 12/05/2018
ms.keywords: MprConfigTransportGetHandle, MprConfigTransportGetHandle function [RAS], _mpr_mprconfigtransportgethandle, mprapi/MprConfigTransportGetHandle, rras.mprconfigtransportgethandle
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
 - MprConfigTransportGetHandle
 - mprapi/MprConfigTransportGetHandle
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
 - MprConfigTransportGetHandle
---

# MprConfigTransportGetHandle function


## -description

The 
<b>MprConfigTransportGetHandle</b> function retrieves a handle to the specified transport protocol's configuration in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. The handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport configuration handle type in the <i>phRouterTransport</i> parameter. Acceptable values for <i>dwTransportId</i> are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Transport (Protocol Family)</th>
</tr>
<tr>
<td>PID_ATALK</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>PID_IP</td>
<td>Internet Protocol version 4</td>
</tr>
<tr>
<td>PID_IPX</td>
<td>Internet Packet Exchange</td>
</tr>
<tr>
<td>PID_NBF</td>
<td>NetBIOS Frames Protocol</td>
</tr>
<tr>
<td>PID_IPV6</td>
<td>Windows Server 2008 or later: Internet Protocol version 6</td>
</tr>
</table>

### -param phRouterTransport [out]

A pointer to a  
<b>HANDLE</b> variable that receives the transport configuration handle type indicated in the <i>dwTransportId</i> parameter.

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
The <i>hMprConfig</i> parameter and/or the <i>phRouterTransport</i> parameter is <b>NULL</b>.

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
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The transport protocol specified by <i>dwTransportId</i> was not found in the router configuration.

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

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>