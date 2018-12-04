---
UID: NF:rpcndr.RpcSsDisableAllocate
title: RpcSsDisableAllocate function
author: windows-sdk-content
description: The RpcSsDisableAllocate function frees resources and memory within the stub memory&#8211;management environment.
old-location: rpc\rpcssdisableallocate.htm
tech.root: rpc
ms.assetid: 08121380-ff75-4f18-aae4-fdd01e1dfa8b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RpcSsDisableAllocate, RpcSsDisableAllocate function [RPC], _rpc_rpcssdisableallocate, rpc.rpcssdisableallocate, rpcndr/RpcSsDisableAllocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - RpcSsDisableAllocate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcSsDisableAllocate function


## -description


The 
<b>RpcSsDisableAllocate</b> function frees resources and memory within the stub memory–management environment.


## -parameters






## -returns



<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcSsDisableAllocate</b> frees all the resources used by a call to 
<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a>. It also releases memory that was allocated by a call to 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a> after the call to 
<b>RpcSsEnableAllocate</b>.


<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a> and 
<b>RpcSsDisableAllocate</b> must be used together as matching pairs.




## -see-also




<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a>
 

 

