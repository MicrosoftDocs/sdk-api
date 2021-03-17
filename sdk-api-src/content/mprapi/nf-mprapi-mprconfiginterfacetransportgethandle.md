---
UID: NF:mprapi.MprConfigInterfaceTransportGetHandle
title: MprConfigInterfaceTransportGetHandle function (mprapi.h)
description: The MprConfigInterfaceTransportGetHandle function retrieves a handle to the transport configuration of an interface in the specified router configuration.
helpviewer_keywords: ["MprConfigInterfaceTransportGetHandle","MprConfigInterfaceTransportGetHandle function [RAS]","_mpr_mprconfiginterfacetransportgethandle","mprapi/MprConfigInterfaceTransportGetHandle","rras.mprconfiginterfacetransportgethandle"]
old-location: rras\mprconfiginterfacetransportgethandle.htm
tech.root: RRAS
ms.assetid: 668ad25c-c5a6-4676-825d-310cc99b321b
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceTransportGetHandle, MprConfigInterfaceTransportGetHandle function [RAS], _mpr_mprconfiginterfacetransportgethandle, mprapi/MprConfigInterfaceTransportGetHandle, rras.mprconfiginterfacetransportgethandle
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
 - MprConfigInterfaceTransportGetHandle
 - mprapi/MprConfigInterfaceTransportGetHandle
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
 - MprConfigInterfaceTransportGetHandle
---

# MprConfigInterfaceTransportGetHandle function


## -description

The 
<b>MprConfigInterfaceTransportGetHandle</b> function retrieves a handle to the transport configuration of an interface in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport configuration handle type in the <i>phRouterIfTransport</i> parameter. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param phRouterIfTransport [out]

A pointer to a  
<b>HANDLE</b> variable that receives the transport configuration handle type for this interface indicated in the <i>dwTransportId</i> parameter.

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
At least one of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>phRouterIfTransport</i> is <b>NULL</b>.</li>
</ul>
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
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface specified by <i>hRouterInterface</i> was not found in the router configuration, or the transport specified by <i>dwTransportId</i> was not enabled on the specified interface.

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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>