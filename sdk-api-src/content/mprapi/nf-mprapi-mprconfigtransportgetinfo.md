---
UID: NF:mprapi.MprConfigTransportGetInfo
title: MprConfigTransportGetInfo function (mprapi.h)
description: The MprConfigTransportGetInfo function retrieves the configuration for the specified transport protocol from the router.
helpviewer_keywords: ["MprConfigTransportGetInfo","MprConfigTransportGetInfo function [RAS]","_mpr_mprconfigtransportgetinfo","mprapi/MprConfigTransportGetInfo","rras.mprconfigtransportgetinfo"]
old-location: rras\mprconfigtransportgetinfo.htm
tech.root: RRAS
ms.assetid: 84054313-f923-47d6-8019-c68a042d2d73
ms.date: 12/05/2018
ms.keywords: MprConfigTransportGetInfo, MprConfigTransportGetInfo function [RAS], _mpr_mprconfigtransportgetinfo, mprapi/MprConfigTransportGetInfo, rras.mprconfigtransportgetinfo
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
 - MprConfigTransportGetInfo
 - mprapi/MprConfigTransportGetInfo
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
 - MprConfigTransportGetInfo
---

# MprConfigTransportGetInfo function


## -description

The 
<b>MprConfigTransportGetInfo</b> function retrieves the configuration for the specified transport protocol from the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterTransport [in]

Handle to the transport protocol configuration being retrieved. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportenum">MprConfigTransportEnum</a>. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

### -param ppGlobalInfo [in, out, optional]

On input, pointer to a pointer variable. 




On output, this pointer variable points to an information header that contains global information for the transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. Free this buffer by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not retrieve the global information.

### -param lpdwGlobalInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the buffer returned through the <i>ppGlobalInfo</i> parameter. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter. However, if <i>ppGlobalInfo</i> is not <b>NULL</b>, this parameter cannot be <b>NULL</b>.

### -param ppClientInterfaceInfo [in, out, optional]

On input, pointer to a pointer variable. 




On output, this pointer points to an information header that contains default interface information for client routers for this transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. Free the buffer by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not retrieve the interface information.

### -param lpdwClientInterfaceInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the buffer returned through the <i>ppClientInterfaceInfo</i> parameter. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter. However, if <i>ppClientInterfaceInfo</i> is not <b>NULL</b>, this parameter cannot be <b>NULL</b>.

### -param lplpwsDLLPath [in, out, optional]

On input, pointer to a pointer to a <b>null</b>-terminated Unicode string. 




On output, the Unicode string receives the name of the router manager DLL for the specified transport.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not retrieve the name of the router manager DLL.

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
<li><i>hMprConfig</i> is <b>NULL</b></li>
<li><i>hRouterTransport</i> is <b>NULL</b></li>
<li><i>ppGlobalInfo</i> is not <b>NULL</b>, but <i>lpdwGlobalInfoSize</i> is <b>NULL</b>.</li>
<li><i>ppClientInterfaceInfo</i> is not <b>NULL</b>, but <i>lpdwClientInterfaceInfo</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The transport protocol configuration that corresponds to <i>hRouterTransport</i> was not found in the router configuration.

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

## -remarks

If the <i>pGlobalInfo</i>, <i>pClientInterfaceInfo</i>, and <i>lpwsDLLPath</i> parameters are all <b>NULL</b>, the function does nothing and returns a value of NO_ERROR.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportenum">MprConfigTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>