---
UID: NF:mprapi.MprConfigInterfaceTransportAdd
title: MprConfigInterfaceTransportAdd function (mprapi.h)
description: The MprConfigInterfaceTransportAdd function adds a transport protocol to an interface configuration on the router.
helpviewer_keywords: ["MprConfigInterfaceTransportAdd","MprConfigInterfaceTransportAdd function [RAS]","_mpr_mprconfiginterfacetransportadd","mprapi/MprConfigInterfaceTransportAdd","rras.mprconfiginterfacetransportadd"]
old-location: rras\mprconfiginterfacetransportadd.htm
tech.root: RRAS
ms.assetid: f4735fd1-031d-4cda-af40-36f55e5796f9
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceTransportAdd, MprConfigInterfaceTransportAdd function [RAS], _mpr_mprconfiginterfacetransportadd, mprapi/MprConfigInterfaceTransportAdd, rras.mprconfiginterfacetransportadd
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
 - MprConfigInterfaceTransportAdd
 - mprapi/MprConfigInterfaceTransportAdd
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
 - MprConfigInterfaceTransportAdd
---

# MprConfigInterfaceTransportAdd function


## -description

The 
<b>MprConfigInterfaceTransportAdd</b> function adds a transport protocol to an interface configuration on the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration to which the specified transport is added. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport to add to the configuration. This parameter also identifies the router manager for the transport. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param lpwsTransportName [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name for the transport being added. If this parameter is not specified and the transport is IP or IPX, 
<b>MprConfigInterfaceTransportAdd</b> uses IP or IPX. If this parameter is not specified and the transport is other than IP or IPX, 
<b>MprConfigInterfaceTransportAdd</b> converts the <i>dwTransportId</i> parameter into a string and uses that as the transport name.

### -param pInterfaceInfo [in]

Pointer to an information header that contains information for the specified interface and transport. The router manager for the specified transport interprets this information. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers.

### -param dwInterfaceInfoSize [in]

Specifies the size, in bytes, of the data pointed to by <i>pInterfaceInfo</i>.

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

In addition to specifying a transport, the <i>dwTransportId</i> parameter also specifies a router manager, because a router maintains a unique router manager for each transport.

If the specified transport already exists, 
<b>MprConfigInterfaceTransportAdd</b> does the equivalent of an 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo">MprConfigInterfaceTransportSetInfo</a> call using the specified parameter values.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_iftransport_0">MPR_IFTRANSPORT_0</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>