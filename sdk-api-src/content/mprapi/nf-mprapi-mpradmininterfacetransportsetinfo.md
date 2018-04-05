---
UID: NF:mprapi.MprAdminInterfaceTransportSetInfo
title: MprAdminInterfaceTransportSetInfo function
author: windows-driver-content
description: The MprAdminInterfaceTransportSetInfo function sets information for a transport running on a specified interface.
old-location: rras\mpradmininterfacetransportsetinfo.htm
old-project: RRAS
ms.assetid: 340610af-6fd8-49e3-947a-e24346a9b888
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: MprAdminInterfaceTransportSetInfo, MprAdminInterfaceTransportSetInfo function [RAS], _mpr_mpradmininterfacetransportsetinfo, mprapi/MprAdminInterfaceTransportSetInfo, rras.mpradmininterfacetransportsetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminInterfaceTransportSetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminInterfaceTransportSetInfo function


## -description


The 
<b>MprAdminInterfaceTransportSetInfo</b> function sets information for a transport running on a specified interface.


## -parameters




### -param hMprServer [in]

Handle to the router on which the transport is being set. Obtain the handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hInterface [in]

Handle to the interface on which the transport is being set. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>.


### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport type to set. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

Pointer to an information header that contains information for the specified interface and transport. Use the 
<a href="https://msdn.microsoft.com/e88720aa-080b-4d87-a442-1b436c256ca6">Information Header Functions</a> to manipulate information headers.


### -param dwInterfaceInfoSize [in]

Specifies the size, in bytes, of the information pointed to by <i>pInterfaceInfo</i>.


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
The <i>pInterfaceInfo</i> parameter is NULL.

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




<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/4e8d7fdf-668e-496a-977a-7a0306173495">MprAdminInterfaceTransportGetInfo</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

