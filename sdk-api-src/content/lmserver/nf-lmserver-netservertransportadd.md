---
UID: NF:lmserver.NetServerTransportAdd
title: NetServerTransportAdd function (lmserver.h)
description: The NetServerTransportAdd function binds the server to the transport protocol.
helpviewer_keywords: ["0","NetServerTransportAdd","NetServerTransportAdd function [Network Management]","_win32_netservertransportadd","lmserver/NetServerTransportAdd","netmgmt.netservertransportadd"]
old-location: netmgmt\netservertransportadd.htm
tech.root: NetMgmt
ms.assetid: c8521aed-0762-4412-b117-c911fc77049b
ms.date: 12/05/2018
ms.keywords: 0, NetServerTransportAdd, NetServerTransportAdd function [Network Management], _win32_netservertransportadd, lmserver/NetServerTransportAdd, netmgmt.netservertransportadd
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetServerTransportAdd
 - lmserver/NetServerTransportAdd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerTransportAdd
---

# NetServerTransportAdd function


## -description

The 
				<b>NetServerTransportAdd</b> function binds the server to the transport protocol.

The extended function 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> allows the calling application to specify the 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>, 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>, and 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a> information levels.

## -parameters

### -param servername [in]

A pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param level [in]

Specifies the information level of the data. This parameter can be the following value. 



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
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
</table>

### -param bufptr [in]

A pointer to the buffer that contains the data.

For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

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
<dt><b>ERROR_DUP_NAME</b></dt>
</dl>
</td>
<td width="60%">
A duplicate name exists on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DOMAINNAME</b></dt>
</dl>
</td>
<td width="60%">
The domain name could not be found on the network.

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
A parameter is invalid. 

This error is returned if the <b>svti0_transportname</b> or <b>svti0_transportaddress</b> member in the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a> structure pointed to by the <i>bufptr</i> parameter is <b>NULL</b>. This error is also returned if the <b>svti0_transportaddresslength</b> member in the <b>SERVER_TRANSPORT_INFO_0</b> structure pointed to by the <i>bufptr</i> parameter is zero or larger than MAX_PATH (defined in the Windef.h header file). 

This error is also returned for other invalid parameters.

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
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerTransportAdd</b> function.

If you add a transport protocol to a server using a call to the 
<b>NetServerTransportAdd</b> function, the connection will not remain after the server reboots or restarts.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportdel">NetServerTransportDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_3">SERVER_TRANSPORT_INFO_3</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>