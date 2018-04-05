---
UID: NF:rpcndr.RpcSsFree
title: RpcSsFree function
author: windows-driver-content
description: The RpcSsFree function releases memory allocated by RpcSsAllocate.
old-location: rpc\rpcssfree.htm
old-project: Rpc
ms.assetid: f004ea19-3d1c-485f-99be-da59cbe478d2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RpcSsFree, RpcSsFree function [RPC], _rpc_rpcssfree, rpc.rpcssfree, rpcndr/RpcSsFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcSsFree
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# RpcSsFree function


## -description


The 
<b>RpcSsFree</b> function releases memory allocated by 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>.


## -parameters




### -param NodeToFree

Pointer to memory allocated by 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a> or 
<a href="https://msdn.microsoft.com/ca3373fa-8ea4-452e-b2a2-f30eb48fef9d">RpcSmAllocate</a>.


## -returns



This function does not return a value.




## -remarks



An application uses 
<b>RpcSsFree</b> to free memory that was allocated with 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>. In cases where the stub allocates the memory for the environment, 
<b>RpcSsFree</b> can also be used to release memory. For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>.

Note that the handle of the thread calling 
<b>RpcSsFree</b> must match the handle of the thread that allocated the memory by calling 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>. Use 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a> and 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a> to pass handles from thread to thread.




## -see-also




<a href="https://msdn.microsoft.com/d8f7fae4-4d91-4f91-9018-c4bcdb4d6c65">RpcSmFree</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a>



<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a>
 

 

