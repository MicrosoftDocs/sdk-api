---
UID: NF:mprapi.MprAdminInterfaceUpdateRoutes
title: MprAdminInterfaceUpdateRoutes function
author: windows-sdk-content
description: The MprAdminInterfaceUpdateRoutes function requests a specified router manager to update its routing information for a specified interface.
old-location: rras\mpradmininterfaceupdateroutes.htm
old-project: rras
ms.assetid: b06ce009-c52f-4d3b-a452-785c75638c89
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MprAdminInterfaceUpdateRoutes, MprAdminInterfaceUpdateRoutes function [RAS], _mpr_mpradmininterfaceupdateroutes, mprapi/MprAdminInterfaceUpdateRoutes, rras.mpradmininterfaceupdateroutes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - MprAdminInterfaceUpdateRoutes
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminInterfaceUpdateRoutes function


## -description


The 
<b>MprAdminInterfaceUpdateRoutes</b> function requests a specified router manager to update its routing information for a specified interface.


## -parameters




### -param hMprServer [in]

Handle to the router on which information is being updated. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hInterface [in]

Handle to the interface being updated. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>.


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
<a href="https://msdn.microsoft.com/df06d847-2448-4a64-bb1b-d60a3eb4f7a8">MprAdminInterfaceQueryUpdateResult</a>.

</td>
</tr>
</table>
 




## -remarks



The <i>dwTransportId</i> parameter specifies both a transport protocol and a unique router manager because the router uses a different router manager for each transport.




## -see-also




<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/df06d847-2448-4a64-bb1b-d60a3eb4f7a8">MprAdminInterfaceQueryUpdateResult</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

