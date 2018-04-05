---
UID: NF:lmserver.NetServerTransportDel
title: NetServerTransportDel function
author: windows-driver-content
description: The NetServerTransportDel function unbinds (or disconnects) the transport protocol from the server. Effectively, the server can no longer communicate with clients using the specified transport protocol (such as TCP or XNS).
old-location: netmgmt\netservertransportdel.htm
old-project: NetMgmt
ms.assetid: 69b22f30-62b1-4dcb-bbb0-aceae8d77f61
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 0, 1, NetServerTransportDel, NetServerTransportDel function [Network Management], _win32_netservertransportdel, lmserver/NetServerTransportDel, netmgmt.netservertransportdel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmserver.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: TIME_OF_DAY_INFO, *PTIME_OF_DAY_INFO, *LPTIME_OF_DAY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetServerTransportDel
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetServerTransportDel function


## -description


The 
				<b>NetServerTransportDel</b> function unbinds (or disconnects) the transport protocol from the server. Effectively, the server can no longer communicate with clients using the specified transport protocol (such as TCP or XNS).


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, and location on the network. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, network location, and domain. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NetNameNotFound</b></dt>
</dl>
</td>
<td width="60%">
The share name does not exist.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerTransportDel</b> function.




## -see-also




<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a>



<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>
 

 

