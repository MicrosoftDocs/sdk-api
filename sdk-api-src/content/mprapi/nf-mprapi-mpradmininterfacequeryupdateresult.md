---
UID: NF:mprapi.MprAdminInterfaceQueryUpdateResult
title: MprAdminInterfaceQueryUpdateResult function
author: windows-sdk-content
description: The MprAdminInterfaceQueryUpdateResult function returns the result of the last request to a specified router manager to update its routes for an interface. For more information, see MprAdminInterfaceUpdateRoutes.
old-location: rras\mpradmininterfacequeryupdateresult.htm
old-project: rras
ms.assetid: df06d847-2448-4a64-bb1b-d60a3eb4f7a8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MprAdminInterfaceQueryUpdateResult, MprAdminInterfaceQueryUpdateResult function [RAS], _mpr_mpradmininterfacequeryupdateresult, mprapi/MprAdminInterfaceQueryUpdateResult, rras.mpradmininterfacequeryupdateresult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminInterfaceQueryUpdateResult
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminInterfaceQueryUpdateResult function


## -description


The 
<b>MprAdminInterfaceQueryUpdateResult</b> function returns the result of the last request to a specified router manager to update its routes for an interface. For more information, see 
<a href="https://msdn.microsoft.com/b06ce009-c52f-4d3b-a452-785c75638c89">MprAdminInterfaceUpdateRoutes</a>.


## -parameters




### -param hMprServer [in]

Handle to the router from which information is being retrieved. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>.


### -param dwProtocolId [in]

A <b>DWORD</b> value that specifies which router manager is being queried. The router uses a different router manager for each transport protocol. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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
 


### -param lpdwUpdateResult [out]

Pointer to a <b>DWORD</b> variable. This variable receives the result of the last call to 
<a href="https://msdn.microsoft.com/b06ce009-c52f-4d3b-a452-785c75638c89">MprAdminInterfaceUpdateRoutes</a>.


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
The specified interface is not connected; the result of the last update is no longer available.

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
The <i>lpdwUpdateResult</i> parameter is <b>NULL</b>.

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
The <i>dwProtocolId</i> value does not match any supported router manager.

</td>
</tr>
</table>
 




## -remarks



The <i>dwProtocolId</i> parameter specifies both a transport and a router manager, since the router maintains a router manager for each transport.




## -see-also




<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/b06ce009-c52f-4d3b-a452-785c75638c89">MprAdminInterfaceUpdateRoutes</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

