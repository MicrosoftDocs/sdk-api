---
UID: NC:rpcdce.RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
title: RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN (rpcdce.h)
description: The RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN is a user-defined callback that can be implemented for each defined interface group. This callback is invoked by the RPC runtime when it detects that the idle state of an interface group has changed.
helpviewer_keywords: ["RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN","RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback","RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback function [RPC]","rpc.rpc_interface_group_idle_callback_fn","rpcdce/RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN"]
old-location: rpc\rpc_interface_group_idle_callback_fn.htm
tech.root: Rpc
ms.assetid: D34F2902-80EE-4011-A837-2A8C21E5A136
ms.date: 12/05/2018
ms.keywords: RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN, RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback, RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback function [RPC], rpc.rpc_interface_group_idle_callback_fn, rpcdce/RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
 - rpcdce/RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rpcdce.h
api_name:
 - RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
---

# RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback function


## -description

The <b>RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</b> is a user-defined callback that can be implemented for each defined interface group.  This callback is invoked by the RPC runtime when it detects that the idle state of an interface group has changed.

## -parameters

### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a> that defines the interface group for which the idle state has changed.

### -param IdleCallbackContext [in]

A user-defined context provided at interface group creation.

### -param IsGroupIdle [in]

<b>TRUE</b> if the interface group has just become idle.  <b>FALSE</b> if the interface group was previously idle but has since received new activity.

## -remarks

When a server registers an interface group, it provides a pointer to an idle callback function through which RPC will notify the application when the interface group’s idle state has changed.  The server application can use this callback to attempt to deactivate the interface group when it becomes idle.


<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a> must not be called from this callback or deadlock can occur.

Note that RPC server activity is not always visible to the server application.  In some cases, simply having a client with an open connection to the server may keep it active even if no calls have been dispatched for a long period of time.  Server applications must not rely on any correlation between the RPC runtime declaring that the group is idle and the time since the last call was dispatched.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupactivate">RpcServerInterfaceGroupActivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupclose">RpcServerInterfaceGroupClose</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupcreate">RpcServerInterfaceGroupCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupdeactivate">RpcServerInterfaceGroupDeactivate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInterfaceGroupInqBindings</a>
