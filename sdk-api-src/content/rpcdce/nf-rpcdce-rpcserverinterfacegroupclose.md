---
UID: NF:rpcdce.RpcServerInterfaceGroupClose
title: RpcServerInterfaceGroupClose function (rpcdce.h)
description: The RpcServerInterfaceGroupClose function is used to free an interface group.
helpviewer_keywords: ["RpcServerInterfaceGroupClose","RpcServerInterfaceGroupClose function [RPC]","rpc.rpcserverinterfacegroupclose","rpcdce/RpcServerInterfaceGroupClose"]
old-location: rpc\rpcserverinterfacegroupclose.htm
tech.root: Rpc
ms.assetid: DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupClose, RpcServerInterfaceGroupClose function [RPC], rpc.rpcserverinterfacegroupclose, rpcdce/RpcServerInterfaceGroupClose
f1_keywords:
- rpcdce/RpcServerInterfaceGroupClose
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcServerInterfaceGroupClose function


## -description


The <b>RpcServerInterfaceGroupClose</b> function is used to free an interface group.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a> that defines the interface group to close.


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
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



If the given interface group is still active, <b>RpcServerInterfaceGroupClose</b> performs a forced deactivation before closing the group.

This function must not be called from an interface group’s idle callback or deadlock can occur.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInterfaceGroupInqBindings</a>
 

 

