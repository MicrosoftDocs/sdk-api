---
UID: NF:mprapi.MprAdminInterfaceTransportAdd
title: MprAdminInterfaceTransportAdd function (mprapi.h)
description: The MprAdminInterfaceTransportAdd function adds a transport (for example, IP or IPX) to a specified interface.
helpviewer_keywords: ["MprAdminInterfaceTransportAdd","MprAdminInterfaceTransportAdd function [RAS]","_mpr_mpradmininterfacetransportadd","mprapi/MprAdminInterfaceTransportAdd","rras.mpradmininterfacetransportadd"]
old-location: rras\mpradmininterfacetransportadd.htm
tech.root: RRAS
ms.assetid: 5978a8d3-78ea-4dc2-a957-32f00c81f52d
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceTransportAdd, MprAdminInterfaceTransportAdd function [RAS], _mpr_mpradmininterfacetransportadd, mprapi/MprAdminInterfaceTransportAdd, rras.mpradmininterfacetransportadd
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
 - MprAdminInterfaceTransportAdd
 - mprapi/MprAdminInterfaceTransportAdd
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
 - MprAdminInterfaceTransportAdd
---

# MprAdminInterfaceTransportAdd function


## -description

The 
<b>MprAdminInterfaceTransportAdd</b> function adds a transport (for example, IP or IPX) to a specified interface.

## -parameters

### -param hMprServer [in]

Handle to the router on which information is being added. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface on which the transport is being added. This handle is obtained by a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport type to add to the interface. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param pInterfaceInfo [in]

Pointer to an information header that specifies interface information for this transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers.

### -param dwInterfaceInfoSize [in]

Specifies the size, in bytes, of the information pointed to by <i>pInterfaceInfo</i>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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
The <i>hInterface</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pInterfaceInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any supported transport.

</td>
</tr>
</table>

## -remarks

The <i>dwTransportId</i> parameter also specifies the router manager because a router uses a different router manager for each transport.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportremove">MprAdminInterfaceTransportRemove</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>