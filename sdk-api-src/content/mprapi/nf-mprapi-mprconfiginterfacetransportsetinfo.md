---
UID: NF:mprapi.MprConfigInterfaceTransportSetInfo
title: MprConfigInterfaceTransportSetInfo function (mprapi.h)
description: The MprConfigInterfaceTransportSetInfo function updates the configuration information for the client on the specified interface and transport protocol.
helpviewer_keywords: ["MprConfigInterfaceTransportSetInfo","MprConfigInterfaceTransportSetInfo function [RAS]","_mpr_mprconfiginterfacetransportsetinfo","mprapi/MprConfigInterfaceTransportSetInfo","rras.mprconfiginterfacetransportsetinfo"]
old-location: rras\mprconfiginterfacetransportsetinfo.htm
tech.root: RRAS
ms.assetid: 1f46b528-d9a1-4967-afa2-424ee1eebbcb
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceTransportSetInfo, MprConfigInterfaceTransportSetInfo function [RAS], _mpr_mprconfiginterfacetransportsetinfo, mprapi/MprConfigInterfaceTransportSetInfo, rras.mprconfiginterfacetransportsetinfo
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
 - MprConfigInterfaceTransportSetInfo
 - mprapi/MprConfigInterfaceTransportSetInfo
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
 - MprConfigInterfaceTransportSetInfo
---

# MprConfigInterfaceTransportSetInfo function


## -description

The 
<b>MprConfigInterfaceTransportSetInfo</b> function updates the configuration information for the client on the specified interface and transport protocol.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration in which to update the information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a> or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param hRouterIfTransport [in]

Handle to the transport configuration in which to update the information for the client. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportadd">MprConfigInterfaceTransportAdd</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

### -param pInterfaceInfo [in, optional]

Pointer to an information header that contains configuration information for the client on the specified interface and transport. The router manager for the specified transport interprets this information. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not update the configuration information for the client.

### -param dwInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the data pointed to by <i>pInterfaceInfo</i>. 




This parameter is optional; the calling application may specify zero for this parameter. However, if <i>pInterfaceInfo</i> is not <b>NULL</b>, this parameter cannot be zero. For more information, see the Remarks section later in this topic.

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
At least one of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>hRouterIfTransport</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface specified by <i>hRouterInterface</i> is no longer present in the router configuration, or the transport specified by <i>hRouterInterface</i> is no longer present on the interface.

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

If the <i>pInterfaceInfo</i> parameter is <b>NULL</b>, 
<b>MprConfigInterfaceTransportSetInfo</b> does nothing and returns immediately with a value of NO_ERROR.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>