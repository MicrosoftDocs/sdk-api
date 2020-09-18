---
UID: NF:lmserver.NetServerComputerNameAdd
title: NetServerComputerNameAdd function (lmserver.h)
description: The NetServerComputerNameAdd function enumerates the transports on which the specified server is active, and binds the emulated server name to each of the transports.
helpviewer_keywords: ["NetServerComputerNameAdd","NetServerComputerNameAdd function [Network Management]","_win32_netservercomputernameadd","lmserver/NetServerComputerNameAdd","netmgmt.netservercomputernameadd"]
old-location: netmgmt\netservercomputernameadd.htm
tech.root: NetMgmt
ms.assetid: 0789fbfe-be91-4849-a31c-1e1a6ae1e70d
ms.date: 12/05/2018
ms.keywords: NetServerComputerNameAdd, NetServerComputerNameAdd function [Network Management], _win32_netservercomputernameadd, lmserver/NetServerComputerNameAdd, netmgmt.netservercomputernameadd
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
 - NetServerComputerNameAdd
 - lmserver/NetServerComputerNameAdd
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
 - NetServerComputerNameAdd
---

# NetServerComputerNameAdd function


## -description

The 
				<b>NetServerComputerNameAdd</b> function enumerates the transports on which the specified server is active, and binds the emulated server name to each of the transports.

<b>NetServerComputerNameAdd</b> is a utility function that combines the functionality of the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a> function and the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.

## -parameters

### -param ServerName [in]

Pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param EmulatedDomainName [in]

Pointer to a string that contains the domain name the specified server should use when announcing its presence using the <i>EmulatedServerName</i>. This parameter is optional.

### -param EmulatedServerName [in]

Pointer to a null-terminated character string that contains the emulated name the server should begin supporting in addition to the name specified by the <i>ServerName</i> parameter.

## -returns

If the function succeeds, the return value is NERR_Success. Note that 
<b>NetServerComputerNameAdd</b> succeeds if the emulated server name specified is added to at least one transport.

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
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerComputerNameAdd</b> function.

The server specified by the <i>ServerName</i> parameter continues to support all names it was supporting, and additionally begins to support new names supplied by successful calls to the 
<b>NetServerComputerNameAdd</b> function.

Name emulation that results from a call to 
<b>NetServerComputerNameAdd</b> ceases when the server reboots or restarts. To discontinue name emulation set by a previous call to 
<b>NetServerComputerNameAdd</b> without restarting or rebooting, you can call the 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a> function.

The 
<b>NetServerComputerNameAdd</b> function is typically used when a system administrator replaces a server, but wants to keep the conversion transparent to users. 


#### Examples

Following is an example of a call to the <b>NetServerComputerNameAdd</b> function requesting that \\Server1 also respond to requests for \\Server2.


```cpp
NetServerComputerNameAdd (Server1, NULL, Server2);

```

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservercomputernamedel">NetServerComputerNameDel</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportadd">NetServerTransportAdd</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportenum">NetServerTransportEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server
		  Functions</a>