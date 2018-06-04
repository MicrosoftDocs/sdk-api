---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NdrAsyncClientCall function


## -description


The <b>NdrAsyncClientCall</b> function is the asynchronous client-side entry point for the <a href="midl._oi">/Oi</a> and <b>/Oic</b> mode stub.


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



