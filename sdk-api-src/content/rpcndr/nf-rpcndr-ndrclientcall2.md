---
UID: NF:rpcndr.NdrClientCall2
title: NdrClientCall2 function
author: windows-sdk-content
description: The NdrClientCall2 function is the client-side entry point for the /Oicf mode stub.
old-location: rpc\ndrclientcall2.htm
tech.root: rpc
ms.assetid: 136b6461-048a-41ee-8514-0dea0861b2c1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: NdrClientCall2, NdrClientCall2 function [RPC], rpc.ndrclientcall2, rpcndr/NdrClientCall2
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
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrClientCall2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NdrClientCall2
: 
---

# NdrClientCall2 function


## -description


The <b>NdrClientCall2</b> function is the client-side entry point for the <a href="https://msdn.microsoft.com/">/Oicf</a> mode stub.


## -parameters




### -param pStubDescriptor [in]

Pointer to the MIDL-generated <a href="https://msdn.microsoft.com/e3178aaa-a30a-43ba-a78a-a28d6f20fa74">MIDL_STUB_DESC</a> structure that contains information about the description of the remote interface.


### -param pFormat [in]

Pointer to the MIDL-generated procedure format string that describes the method and parameters.


### -param arg3 [in, out]

Pointer to the client-side calling stack.


## -returns



Return value of the remote call. The maximum size of a return value is equivalent to the register size of the system. MIDL switches to the <a href="https://msdn.microsoft.com/dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb">/Os</a> mode stub if the return value size is larger than the register size.

Depending on the method definition, this function can throw an exception if there is a network or server failure.




## -remarks



The <b>NdrClientCall2</b> function is used by all <a href="https://msdn.microsoft.com/">/Oicf</a> mode client-side stubs. The <b>NdrClientCall2</b> function transmits all [in] data to the remote server, and upon receipt of the response packet, returns the [out] value to the client-side application.



