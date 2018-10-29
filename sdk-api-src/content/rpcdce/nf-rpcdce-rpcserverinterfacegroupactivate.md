---
UID: NF:rpcdce.RpcServerInterfaceGroupActivate
title: RpcServerInterfaceGroupActivate function
author: windows-sdk-content
description: The RpcServerInterfaceGroupActivate function tells the RPC server runtime to register the interface group’s interfaces and endpoints and begin listening for calls.
old-location: rpc\rpcserverinterfacegroupactivate.htm
tech.root: Rpc
ms.assetid: A467DDEC-BEB1-4050-B540-4A1E819E7373
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcServerInterfaceGroupActivate, RpcServerInterfaceGroupActivate function [RPC], rpc.rpcserverinterfacegroupactivate, rpcdce/RpcServerInterfaceGroupActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerInterfaceGroupActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerInterfaceGroupActivate function


## -description


The <b>RpcServerInterfaceGroupActivate</b> function tells the RPC server runtime to register the interface group’s interfaces and endpoints and begin listening for calls.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a> that defines the interface group to activate.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is not supported on this host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_RPC_PROTSEQ</b></dt>
</dl>
</td>
<td width="60%">
The protocol sequence is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ENDPOINT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The endpoint format is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_SECURITY_DESC</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor for an endpoint or interface is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcServerInterfaceGroupActivate</b> does the bulk of the initialization work that the RPC server applications need to do.  It performs the following operations:<ul>
<li>Instructs the RPC runtime to begin listening for calls.</li>
<li>Registers the endpoints with the server runtime.</li>
<li>Registers the interfaces with the server runtime.</li>
<li>Registers the endpoints and interfaces with the RPC endpoint mapper.</li>
</ul>


<b>RpcServerInterfaceGroupActivate</b> is atomic.  If at any point the operation fails, any items that were previously registered are undone.  

Calls may be dispatched to the server application before this function returns.




## -see-also




<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInterfaceGroupInqBindings</a>
 

 

