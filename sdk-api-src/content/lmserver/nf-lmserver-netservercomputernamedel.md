---
UID: NF:lmserver.NetServerComputerNameDel
title: NetServerComputerNameDel function (lmserver.h)
description: The NetServerComputerNameDel function causes the specified server to cease supporting the emulated server name set by a previous call to the NetServerComputerNameAdd function. The function does this by unbinding network transports from the emulated name.
helpviewer_keywords: ["NetServerComputerNameDel","NetServerComputerNameDel function [Network Management]","_win32_netservercomputernamedel","lmserver/NetServerComputerNameDel","netmgmt.netservercomputernamedel"]
old-location: netmgmt\netservercomputernamedel.htm
tech.root: NetMgmt
ms.assetid: 501232ad-2821-4bbd-9f16-0f49984f6101
ms.date: 12/05/2018
ms.keywords: NetServerComputerNameDel, NetServerComputerNameDel function [Network Management], _win32_netservercomputernamedel, lmserver/NetServerComputerNameDel, netmgmt.netservercomputernamedel
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
 - NetServerComputerNameDel
 - lmserver/NetServerComputerNameDel
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
 - NetServerComputerNameDel
---

# NetServerComputerNameDel function


## -description

The 
				<b>NetServerComputerNameDel</b> function causes the specified server to cease supporting the emulated server name set by a previous call to the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a> function. The function does this by unbinding network transports from the emulated name.

## -parameters

### -param ServerName [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param EmulatedServerName [in]

Pointer to a null-terminated character string that contains the emulated name the server should stop supporting. The server continues to support all other server names it was supporting.

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
<b>NetServerComputerNameDel</b> function.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernameadd">NetServerComputerNameAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server
		  Functions</a>