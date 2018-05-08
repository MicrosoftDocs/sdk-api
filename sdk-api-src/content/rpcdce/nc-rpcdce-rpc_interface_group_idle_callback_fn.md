---
UID: NC:rpcdce.RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
title: RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
author: windows-driver-content
description: The RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN is a user-defined callback that can be implemented for each defined interface group. This callback is invoked by the RPC runtime when it detects that the idle state of an interface group has changed.
old-location: rpc\rpc_interface_group_idle_callback_fn.htm
old-project: Rpc
ms.assetid: D34F2902-80EE-4011-A837-2A8C21E5A136
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN, RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback, RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback function [RPC], rpc.rpc_interface_group_idle_callback_fn, rpcdce/RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Rpcdce.h
api_name:
-	RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN callback function


## -description


The <b>RPC_INTERFACE_GROUP_IDLE_CALLBACK_FN</b> is a user-defined callback that can be implemented for each defined interface group.  This callback is invoked by the RPC runtime when it detects that the idle state of an interface group has changed.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a> that defines the interface group for which the idle state has changed.


### -param *IdleCallbackContext [in]

A user-defined context provided at interface group creation.


### -param IsGroupIdle [in]

<b>TRUE</b> if the interface group has just become idle.  <b>FALSE</b> if the interface group was previously idle but has since received new activity.  


## -returns



This callback function does not return a value.




## -remarks



When a server registers an interface group, it provides a pointer to an idle callback function through which RPC will notify the application when the interface group’s idle state has changed.  The server application can use this callback to attempt to deactivate the interface group when it becomes idle.


<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a> must not be called from this callback or deadlock can occur.

Note that RPC server activity is not always visible to the server application.  In some cases, simply having a client with an open connection to the server may keep it active even if no calls have been dispatched for a long period of time.  Server applications must not rely on any correlation between the RPC runtime declaring that the group is idle and the time since the last call was dispatched.




## -see-also




<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/625D8E6E-278F-4A96-879B-64294531D21B">RpcServerInterfaceGroupDeactivate</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInterfaceGroupInqBindings</a>
 

 

