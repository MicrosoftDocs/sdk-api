---
UID: NF:mprapi.MprAdminInterfaceUpdateRoutes
title: MprAdminInterfaceUpdateRoutes function (mprapi.h)
description: The MprAdminInterfaceUpdateRoutes function requests a specified router manager to update its routing information for a specified interface.
helpviewer_keywords: ["MprAdminInterfaceUpdateRoutes","MprAdminInterfaceUpdateRoutes function [RAS]","_mpr_mpradmininterfaceupdateroutes","mprapi/MprAdminInterfaceUpdateRoutes","rras.mpradmininterfaceupdateroutes"]
old-location: rras\mpradmininterfaceupdateroutes.htm
tech.root: RRAS
ms.assetid: b06ce009-c52f-4d3b-a452-785c75638c89
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceUpdateRoutes, MprAdminInterfaceUpdateRoutes function [RAS], _mpr_mpradmininterfaceupdateroutes, mprapi/MprAdminInterfaceUpdateRoutes, rras.mpradmininterfaceupdateroutes
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
 - MprAdminInterfaceUpdateRoutes
 - mprapi/MprAdminInterfaceUpdateRoutes
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
 - MprAdminInterfaceUpdateRoutes
---

# MprAdminInterfaceUpdateRoutes function


## -description

The 
<b>MprAdminInterfaceUpdateRoutes</b> function requests a specified router manager to update its routing information for a specified interface.

## -parameters

### -param hMprServer [in]

Handle to the router on which information is being updated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface being updated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param dwProtocolId [in]

A <b>DWORD</b> value that specifies which router manager is updating its routing information. The router uses a different router manager for each transport protocol. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param hEvent [in]

Handle to an event that is signaled when the attempt to update routing information for the specified interface has completed. If <b>NULL</b>, then the function is synchronous. The calling application must specify <b>NULL</b> for this parameter, if <i>hMprServer</i> specifies a remote router.

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
<dt><b>ERROR_INTERFACE_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified interface is not connected. Therefore, routes cannot be updated.

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
The <i>dwTransportId</i> value does not match any of the router managers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UPDATE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A routing information update operation is already in progress on this interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PENDING</b></dt>
</dl>
</td>
<td width="60%">
The interface is in the process of updating routing information. The calling application must wait on the event object specified by <i>hEvent</i>. After the event is signaled, the status of the update operation can be obtained by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacequeryupdateresult">MprAdminInterfaceQueryUpdateResult</a>.

</td>
</tr>
</table>

## -remarks

The <i>dwTransportId</i> parameter specifies both a transport protocol and a unique router manager because the router uses a different router manager for each transport.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacequeryupdateresult">MprAdminInterfaceQueryUpdateResult</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>