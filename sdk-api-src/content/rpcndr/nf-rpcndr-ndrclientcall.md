---
UID: NF:rpcndr.NdrClientCall
title: NdrClientCall function
author: windows-sdk-content
description: The NdrClientCall function is the client-side entry point for the /Oicf mode stub.
old-location: rpc\ndrclientcall.htm
old-project: rpc
ms.assetid: c7bf480a-a9c7-4d67-a7b6-cba6352b4600
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrClientCall, NdrClientCall function [RPC], rpc.ndrclientcall, rpcndr/NdrClientCall
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrClientCall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrClientCall function


## -description


The <b>NdrClientCall</b> function is the client-side entry point for the <a href="https://msdn.microsoft.com/">/Oicf</a> mode stub.


## -parameters




### -param pStubDescriptor [in]

Pointer to the MIDL-generated <a href="https://msdn.microsoft.com/e3178aaa-a30a-43ba-a78a-a28d6f20fa74">MIDL_STUB_DESC</a> structure that contains information about the description of the remote interface.


### -param pFormat [in]

Pointer to the MIDL-generated procedure format string that describes the method and parameters.


### -param param

TBD




####### - ... [in, out]

Pointer to the client-side calling stack.


## -returns



Return value of the remote call. The maximum size of a return value is equivalent to the register size of the system. MIDL switches to the <a href="https://msdn.microsoft.com/dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb">/Os</a> mode stub if the return value size is larger than the register size.

Depending on the method definition, this function can throw an exception if there is a network or server failure.




## -remarks



The <b>NdrClientCall</b> function is used by the <a href="https://msdn.microsoft.com/">/Oicf /robust</a>  client-side stub. The <b>/Oi</b> and <b>/Oic</b> client-side stubs are obsolete as of MIDL version 6.0.359 and should not be used. The <b>NdrClientCall</b> function transmits all [in] data to the remote server, and upon receipt of the response packet, returns the [out] value to the client-side application.




## -see-also




<a href="https://msdn.microsoft.com/">/Oicf</a>



<a href="https://msdn.microsoft.com/7a858600-ea06-4396-9a1b-240d646e8c7d">/robust</a>
 

 

