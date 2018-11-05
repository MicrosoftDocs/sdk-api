---
UID: NF:rpcdce.RpcServerInterfaceGroupInqBindings
title: RpcServerInterfaceGroupInqBindings function
author: windows-sdk-content
description: The RpcServerInterfaceGroupInqBindings function returns the binding handles over which remote procedure calls can be received for the given interface group.
old-location: rpc\rpcserverinterfacegroupinqbindings.htm
tech.root: rpc
ms.assetid: 90535A05-9835-45F2-A62F-718736A80ED3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RpcServerInterfaceGroupInqBindings, RpcServerInterfaceGroupInqBindings function [RPC], rpc.rpcserverinterfacegroupinqbindings, rpcdce/RpcServerInterfaceGroupInqBindings
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
 - RpcServerInterfaceGroupInqBindings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerInterfaceGroupInqBindings function


## -description


The <b>RpcServerInterfaceGroupInqBindings</b> function returns the binding handles over which remote procedure calls can be received for the given interface group.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a> that defines the interface group for which the bindings should be queried.


### -param BindingVector [out]

Returns a pointer to a pointer to a vector of server binding handles.


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
<dt><b>RPC_S_NO_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
There are no bindings.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls <b>RpcServerInterfaceGroupInqBindings</b> to obtain a vector of server binding handles for the given interface group. The RPC run-time library creates binding handles for an interface group when a server application calls the <a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a> function.

The returned binding vector can contain binding handles with dynamic endpoints or binding handles with well-known endpoints, depending on the interface group’s endpoint specification.

A server uses the vector of binding handles for exporting to the name service or for conversion to string bindings.  If there are no binding handles (no registered protocol sequences), <b>RpcServerInterfaceGroupInqBindings</b> returns <b>RPC_S_NO_BINDINGS</b>and <i>BindingVector</i> is <b>NULL</b>. The server is responsible for calling <a href="https://msdn.microsoft.com/a8af56ae-bacc-497d-b65e-c0a56f3b09de">RpcBindingVectorFree</a> to release the vector's memory.




## -see-also




<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>
 

 

