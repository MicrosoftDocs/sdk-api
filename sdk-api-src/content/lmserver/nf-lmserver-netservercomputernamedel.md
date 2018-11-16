---
UID: NF:lmserver.NetServerComputerNameDel
title: NetServerComputerNameDel function
author: windows-sdk-content
description: The NetServerComputerNameDel function causes the specified server to cease supporting the emulated server name set by a previous call to the NetServerComputerNameAdd function. The function does this by unbinding network transports from the emulated name.
old-location: netmgmt\netservercomputernamedel.htm
tech.root: NetMgmt
ms.assetid: 501232ad-2821-4bbd-9f16-0f49984f6101
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: NetServerComputerNameDel, NetServerComputerNameDel function [Network Management], _win32_netservercomputernamedel, lmserver/NetServerComputerNameDel, netmgmt.netservercomputernamedel
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerComputerNameDel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetServerComputerNameDel
: 
---

# NetServerComputerNameDel function


## -description


The 
				<b>NetServerComputerNameDel</b> function causes the specified server to cease supporting the emulated server name set by a previous call to the 
<a href="https://msdn.microsoft.com/0789fbfe-be91-4849-a31c-1e1a6ae1e70d">NetServerComputerNameAdd</a> function. The function does this by unbinding network transports from the emulated name.


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




<a href="https://msdn.microsoft.com/0789fbfe-be91-4849-a31c-1e1a6ae1e70d">NetServerComputerNameAdd</a>



<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a>



<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server
		  Functions</a>
 

 

