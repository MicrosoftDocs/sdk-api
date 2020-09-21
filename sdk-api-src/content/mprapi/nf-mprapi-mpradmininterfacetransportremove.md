---
UID: NF:mprapi.MprAdminInterfaceTransportRemove
title: MprAdminInterfaceTransportRemove function (mprapi.h)
description: The MprAdminInterfaceTransportRemove function removes a transport (for example, IP or IPX) from a specified interface.
helpviewer_keywords: ["MprAdminInterfaceTransportRemove","MprAdminInterfaceTransportRemove function [RAS]","_mpr_mpradmininterfacetransportremove","mprapi/MprAdminInterfaceTransportRemove","rras.mpradmininterfacetransportremove"]
old-location: rras\mpradmininterfacetransportremove.htm
tech.root: RRAS
ms.assetid: 0773923a-6bfe-4b86-a8ca-a52016733668
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceTransportRemove, MprAdminInterfaceTransportRemove function [RAS], _mpr_mpradmininterfacetransportremove, mprapi/MprAdminInterfaceTransportRemove, rras.mpradmininterfacetransportremove
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
 - MprAdminInterfaceTransportRemove
 - mprapi/MprAdminInterfaceTransportRemove
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
 - MprAdminInterfaceTransportRemove
---

# MprAdminInterfaceTransportRemove function


## -description

The 
<b>MprAdminInterfaceTransportRemove</b> function removes a transport (for example, IP or IPX) from a specified interface.

## -parameters

### -param hMprServer [in]

Handle to the router from which the transport is being removed. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface from which the transport is being removed. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport type to remove. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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
<dt><b>ERROR_INTERFACE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The interface specified is a demand-dial interface and is currently connected.

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
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any supported transport.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportadd">MprAdminInterfaceTransportAdd</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>