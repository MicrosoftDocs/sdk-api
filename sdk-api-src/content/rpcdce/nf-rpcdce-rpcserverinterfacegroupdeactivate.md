---
UID: NF:rpcdce.RpcServerInterfaceGroupDeactivate
title: RpcServerInterfaceGroupDeactivate function (rpcdce.h)
description: The RpcServerInterfaceGroupDeactivate function tells the RPC runtime to attempt to close the given interface group, optionally aborting the operation if there is outstanding client activity.
helpviewer_keywords: ["RpcServerInterfaceGroupDeactivate","RpcServerInterfaceGroupDeactivate function [RPC]","rpc.rpcserverinterfacegroupdeactivate","rpcdce/RpcServerInterfaceGroupDeactivate"]
old-location: rpc\rpcserverinterfacegroupdeactivate.htm
tech.root: Rpc
ms.assetid: 625D8E6E-278F-4A96-879B-64294531D21B
ms.date: 12/05/2018
ms.keywords: RpcServerInterfaceGroupDeactivate, RpcServerInterfaceGroupDeactivate function [RPC], rpc.rpcserverinterfacegroupdeactivate, rpcdce/RpcServerInterfaceGroupDeactivate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcServerInterfaceGroupDeactivate
 - rpcdce/RpcServerInterfaceGroupDeactivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerInterfaceGroupDeactivate
---

# RpcServerInterfaceGroupDeactivate function


## -description

The <b>RpcServerInterfaceGroupDeactivate</b> function tells the RPC runtime to attempt to close the given interface group, optionally aborting the operation if there is outstanding client activity.

## -parameters

### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a> that defines the interface group to deactivate

### -param ForceDeactivation [in]

If <b>TRUE</b>, the RPC runtime should ignore client activity and unconditionally deactivate the interface group.  If <b>FALSE</b>, the operation should be aborted if new activity takes place.

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
<dt><b>RPC_S_SERVER_TOO_BUSY</b></dt>
</dl>
</td>
<td width="60%">
<i>ForceDeactivation</i> is <b>FALSE</b> and there is outstanding client activity.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcServerInterfaceGroupDeactivate</b> is used by server applications to unregister the interfaces and endpoints in an interface group.  It does the bulk of the shutdown work that RPC server applications need to do.  It performs the following operations:<ul>
<li>Unregisters the endpoints and interfaces from the RPC endpoint mapper.</li>
<li>Unregisters the endpoints from the server runtime.</li>
<li>Unregisters the interfaces from the server runtime.  </li>
<li>Tells the runtime to stop listening for calls if no other interfaces are present.</li>
</ul>


If <i>ForceDeactivation</i> is <b>FALSE</b>, <b>RpcServerInterfaceGroupDeactivate</b> will only deactivate the interface group if there is no outstanding client activity.  If new activity arrives during the deactivation process, <b>RPC_S_SERVER_TOO_BUSY</b> is returned.  In this case, the operation is rolled back and the interface group will continue to receive and dispatch calls.

If <i>ForceDeactivation</i> is <b>TRUE</b>, <b>RpcServerInterfaceGroupDeactivate</b> does not fail.

Service applications can call <b>RpcServerInterfaceGroupDeactivate</b> with <i>ForceDeactivation</i> set to <b>FALSE</b> from their idle callback function <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>.  When used in conjunction with RPC service start triggers, this enables them to safely idle stop without missing calls from potential clients.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInterfaceGroupInqBindings</a>