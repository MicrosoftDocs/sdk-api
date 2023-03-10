---
UID: NF:lmserver.NetServerTransportDel
title: NetServerTransportDel function (lmserver.h)
description: The NetServerTransportDel function unbinds (or disconnects) the transport protocol from the server. Effectively, the server can no longer communicate with clients using the specified transport protocol (such as TCP or XNS).
helpviewer_keywords: ["0","1","NetServerTransportDel","NetServerTransportDel function [Network Management]","_win32_netservertransportdel","lmserver/NetServerTransportDel","netmgmt.netservertransportdel"]
old-location: netmgmt\netservertransportdel.htm
tech.root: NetMgmt
ms.assetid: 69b22f30-62b1-4dcb-bbb0-aceae8d77f61
ms.date: 12/05/2018
ms.keywords: 0, 1, NetServerTransportDel, NetServerTransportDel function [Network Management], _win32_netservertransportdel, lmserver/NetServerTransportDel, netmgmt.netservertransportdel
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
 - NetServerTransportDel
 - lmserver/NetServerTransportDel
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
 - NetServerTransportDel
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
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, network location, and domain. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a> structure.

</td>
</tr>
</table>

### -param bufptr [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
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

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>