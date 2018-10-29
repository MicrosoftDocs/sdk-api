---
UID: NF:rpcdce.RpcServerInterfaceGroupClose
title: RpcServerInterfaceGroupClose function
author: windows-sdk-content
description: The RpcServerInterfaceGroupClose function is used to free an interface group.
old-location: rpc\rpcserverinterfacegroupclose.htm
tech.root: Rpc
ms.assetid: DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcServerInterfaceGroupClose, RpcServerInterfaceGroupClose function [RPC], rpc.rpcserverinterfacegroupclose, rpcdce/RpcServerInterfaceGroupClose
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
 - RpcServerInterfaceGroupClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerInterfaceGroupClose function


## -description


The <b>RpcServerInterfaceGroupClose</b> function is used to free an interface group.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a> that defines the interface group to close.


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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
<i>IfGroup</i> is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



If the given interface group is still active, <b>RpcServerInterfaceGroupClose</b> performs a forced deactivation before closing the group.

This function must not be called from an interface group’s idle callback or deadlock can occur.




## -see-also




<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInterfaceGroupInqBindings</a>
 

 

