---
UID: NF:mprapi.MprAdminInterfaceTransportGetInfo
title: MprAdminInterfaceTransportGetInfo function (mprapi.h)
description: The MprAdminInterfaceTransportGetInfo function retrieves information about a transport running on a specified interface.
helpviewer_keywords: ["MprAdminInterfaceTransportGetInfo","MprAdminInterfaceTransportGetInfo function [RAS]","_mpr_mpradmininterfacetransportgetinfo","mprapi/MprAdminInterfaceTransportGetInfo","rras.mpradmininterfacetransportgetinfo"]
old-location: rras\mpradmininterfacetransportgetinfo.htm
tech.root: RRAS
ms.assetid: 4e8d7fdf-668e-496a-977a-7a0306173495
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceTransportGetInfo, MprAdminInterfaceTransportGetInfo function [RAS], _mpr_mpradmininterfacetransportgetinfo, mprapi/MprAdminInterfaceTransportGetInfo, rras.mpradmininterfacetransportgetinfo
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
 - MprAdminInterfaceTransportGetInfo
 - mprapi/MprAdminInterfaceTransportGetInfo
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
 - MprAdminInterfaceTransportGetInfo
---

# MprAdminInterfaceTransportGetInfo function


## -description

The 
<b>MprAdminInterfaceTransportGetInfo</b> function retrieves information about a transport running on a specified interface.

## -parameters

### -param hMprServer [in]

Handle to the router from which information is being retrieved. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport for which information is requested. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param ppInterfaceInfo [out]

Pointer to a pointer variable. The pointer variable points to an information header that receives information for the specified interface and transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

### -param lpdwInterfaceInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size in bytes of the interface information returned through the <i>ppInterfaceInfo</i> parameter. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the size of the interface information.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid, or if the interface specified is administratively disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The specified transport is not running on the specified interface.

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
The <i>dwTransportId</i> value does not match any supported transports.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportsetinfo">MprAdminInterfaceTransportSetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>