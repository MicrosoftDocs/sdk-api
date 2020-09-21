---
UID: NF:mprapi.MprConfigInterfaceTransportRemove
title: MprConfigInterfaceTransportRemove function (mprapi.h)
description: The MprConfigInterfaceTransportRemove function removes the specified transport from the specified interface configuration on the router.
helpviewer_keywords: ["MprConfigInterfaceTransportRemove","MprConfigInterfaceTransportRemove function [RAS]","_mpr_mprconfiginterfacetransportremove","mprapi/MprConfigInterfaceTransportRemove","rras.mprconfiginterfacetransportremove"]
old-location: rras\mprconfiginterfacetransportremove.htm
tech.root: RRAS
ms.assetid: 0f286003-f9d8-490b-a379-76baa3f53c6f
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceTransportRemove, MprConfigInterfaceTransportRemove function [RAS], _mpr_mprconfiginterfacetransportremove, mprapi/MprConfigInterfaceTransportRemove, rras.mprconfiginterfacetransportremove
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
 - MprConfigInterfaceTransportRemove
 - mprapi/MprConfigInterfaceTransportRemove
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
 - MprConfigInterfaceTransportRemove
---

# MprConfigInterfaceTransportRemove function


## -description

The 
<b>MprConfigInterfaceTransportRemove</b> function removes the specified transport from the specified interface configuration on the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. The handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration from which to delete the specified transport. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param hRouterIfTransport [in]

Handle to the interface transport configuration to be deleted. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportadd">MprConfigInterfaceTransportAdd</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

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
One of the following is true: 




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



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportadd">MprConfigInterfaceTransportAdd</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgethandle">MprConfigInterfaceTransportGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>