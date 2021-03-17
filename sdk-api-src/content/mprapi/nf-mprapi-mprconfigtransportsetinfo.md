---
UID: NF:mprapi.MprConfigTransportSetInfo
title: MprConfigTransportSetInfo function (mprapi.h)
description: The MprConfigTransportSetInfo function changes the configuration for the specified transport protocol in the specified router configuration.
helpviewer_keywords: ["MprConfigTransportSetInfo","MprConfigTransportSetInfo function [RAS]","_mpr_mprconfigtransportsetinfo","mprapi/MprConfigTransportSetInfo","rras.mprconfigtransportsetinfo"]
old-location: rras\mprconfigtransportsetinfo.htm
tech.root: RRAS
ms.assetid: 571149a5-5a09-4a04-9327-47aecca7d17f
ms.date: 12/05/2018
ms.keywords: MprConfigTransportSetInfo, MprConfigTransportSetInfo function [RAS], _mpr_mprconfigtransportsetinfo, mprapi/MprConfigTransportSetInfo, rras.mprconfigtransportsetinfo
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
 - MprConfigTransportSetInfo
 - mprapi/MprConfigTransportSetInfo
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
 - MprConfigTransportSetInfo
---

# MprConfigTransportSetInfo function


## -description

The 
<b>MprConfigTransportSetInfo</b> function changes the configuration for the specified transport protocol in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterTransport [in]

Handle to the transport protocol configuration being updated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportenum">MprConfigTransportEnum</a>. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

### -param pGlobalInfo [in, optional]

Pointer to an information header that specifies global information for the transport protocol. The router manager for the transport interprets this information. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter.

### -param dwGlobalInfoSize [in, optional]

Specifies the size, in bytes, of the data pointed to by <i>pGlobalInfo</i>. If the calling application specifies <b>NULL</b> for <i>pGlobalInfo</i>, the calling application should specify zero for this parameter.

### -param pClientInterfaceInfo [in, optional]

Pointer to an information header that specifies default interface information for client routers. The information is used to configure dynamic interfaces for client routers for this transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. 




This parameter is optional; the calling application can specify <b>NULL</b> for this parameter.

### -param dwClientInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the data pointed to by <i>pClientInterfaceInfo</i>. If the calling application specifies <b>NULL</b> for <i>pClientInterfaceInfo</i>, the calling application should specify zero for this parameter.

### -param lpwsDLLPath [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the router manager DLL for the specified transport. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter.

## -returns

If the function succeeds, the return value is NO_ERROR. For more information, see the Remarks section later in this topic.

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
The <i>hMprConfig</i> parameter is <b>NULL</b>, the <i>hRouterTransport</i> parameter is <b>NULL</b>, or both are <b>NULL</b>.

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

## -remarks

Use 
<b>MprConfigTransportSetInfo</b> to set the transport's global information, default interface information, or the name of the router manager DLL for the transport.

<b>MprConfigTransportSetInfo</b> attempts to set the items in the order in which they appear in the parameter list:

<ol>
<li>Global information.</li>
<li>Default interface information for client routers.</li>
<li>Router manager DLL name.</li>
</ol>
If 
<b>MprConfigTransportSetInfo</b> is unable to set any one of the items, it returns immediately without attempting to set the remaining items.

If the <i>pGlobalInfo</i>, <i>pClientInterfaceInfo</i>, and <i>lpwsDLLPath</i> parameters are all <b>NULL</b>, the function does nothing, returning a value of NO_ERROR.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportcreate">MprConfigTransportCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportenum">MprConfigTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgethandle">MprConfigTransportGetHandle</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>