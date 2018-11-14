---
UID: NF:lmserver.NetServerComputerNameAdd
title: NetServerComputerNameAdd function
author: windows-sdk-content
description: The NetServerComputerNameAdd function enumerates the transports on which the specified server is active, and binds the emulated server name to each of the transports.
old-location: netmgmt\netservercomputernameadd.htm
tech.root: NetMgmt
ms.assetid: 0789fbfe-be91-4849-a31c-1e1a6ae1e70d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetServerComputerNameAdd, NetServerComputerNameAdd function [Network Management], _win32_netservercomputernameadd, lmserver/NetServerComputerNameAdd, netmgmt.netservercomputernameadd
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
 - NetServerComputerNameAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetServerComputerNameAdd
: 
---

# NetServerComputerNameAdd function


## -description


The 
				<b>NetServerComputerNameAdd</b> function enumerates the transports on which the specified server is active, and binds the emulated server name to each of the transports.

<b>NetServerComputerNameAdd</b> is a utility function that combines the functionality of the 
<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a> function and the 
<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function.


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
<a href="https://msdn.microsoft.com/501232ad-2821-4bbd-9f16-0f49984f6101">NetServerComputerNameDel</a> function.

The 
<b>NetServerComputerNameAdd</b> function is typically used when a system administrator replaces a server, but wants to keep the conversion transparent to users. 


#### Examples

Following is an example of a call to the <b>NetServerComputerNameAdd</b> function requesting that \\Server1 also respond to requests for \\Server2.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>NetServerComputerNameAdd (Server1, NULL, Server2);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/501232ad-2821-4bbd-9f16-0f49984f6101">NetServerComputerNameDel</a>



<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a>



<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server
		  Functions</a>
 

 

