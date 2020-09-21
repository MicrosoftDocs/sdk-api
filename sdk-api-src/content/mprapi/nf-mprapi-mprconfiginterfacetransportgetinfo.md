---
UID: NF:mprapi.MprConfigInterfaceTransportGetInfo
title: MprConfigInterfaceTransportGetInfo function (mprapi.h)
description: The MprConfigInterfaceTransportGetInfo function retrieves the configuration information for the specified client on the specified interface.
helpviewer_keywords: ["MprConfigInterfaceTransportGetInfo","MprConfigInterfaceTransportGetInfo function [RAS]","_mpr_mprconfiginterfacetransportgetinfo","mprapi/MprConfigInterfaceTransportGetInfo","rras.mprconfiginterfacetransportgetinfo"]
old-location: rras\mprconfiginterfacetransportgetinfo.htm
tech.root: RRAS
ms.assetid: 2b0bb412-a480-43ff-b29a-cf4e7674d2c4
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceTransportGetInfo, MprConfigInterfaceTransportGetInfo function [RAS], _mpr_mprconfiginterfacetransportgetinfo, mprapi/MprConfigInterfaceTransportGetInfo, rras.mprconfiginterfacetransportgetinfo
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
 - MprConfigInterfaceTransportGetInfo
 - mprapi/MprConfigInterfaceTransportGetInfo
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
 - MprConfigInterfaceTransportGetInfo
---

# MprConfigInterfaceTransportGetInfo function


## -description

The 
<b>MprConfigInterfaceTransportGetInfo</b> function retrieves the configuration information for the specified client on the specified interface.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration from which to retrieve the specified client information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param hRouterIfTransport [in]

Handle to the transport configuration from which to retrieve the specified client information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportadd">MprConfigInterfaceTransportAdd</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

### -param ppInterfaceInfo [in, out, optional]

On input, pointer to a pointer variable. 




On output, this pointer variable points to an information header that contains configuration information for the client. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the configuration information.

### -param lpdwInterfaceInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the data pointed to by <i>ppInterfaceInfo</i>. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter. However, if <i>ppInterfaceInfo</i> is not <b>NULL</b>, this parameter cannot be <b>NULL</b>. For more information, see the Remarks section later in this topic.

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
One of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>hRouterIfTransport</i> is <b>NULL</b>.</li>
<li><i>ppInterfaceInfo</i> is not <b>NULL</b>, but <i>lpdwInterfaceInfoSize</i> is <b>NULL</b>.</li>
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
The interface specified by <i>hRouterIfTransport</i> was not found in the router configuration, or the transport specified by <i>hRouterIfTransport</i> was not enabled on the specified interface.

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

## -remarks

If the <i>ppInterfaceInfo</i> parameter is <b>NULL</b>, 
<b>MprConfigInterfaceTransportGetInfo</b> does nothing and returns immediately with a value of NO_ERROR.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_iftransport_0">MPR_IFTRANSPORT_0</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>