---
UID: NC:routprot.PREGISTER_PROTOCOL
title: PREGISTER_PROTOCOL
author: windows-sdk-content
description: The RegisterProtocol function registers the routing protocol with the router manager. It also informs the router manager of the functionality that the routing protocol supports.
old-location: rras\registerprotocol.htm
tech.root: rras
ms.assetid: b9027ef9-e573-4df0-b37e-d09956c1f8ee
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: PREGISTER_PROTOCOL, PREGISTER_PROTOCOL callback, RegisterProtocol, RegisterProtocol callback function [RAS], _mpr_registerprotocol, routprot/RegisterProtocol, rras.registerprotocol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - RegisterProtocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PREGISTER_PROTOCOL callback function


## -description


The 
<b>RegisterProtocol</b> function registers the routing protocol with the router manager. It also informs the router manager of the functionality that the routing protocol supports.


## -parameters




### -param pRoutingChar [in, out]

On input, pointer to an 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a> structure. 




On output, receives pointers to functions implemented for the routing protocol.

See the reference page for the 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a> structure for more information on how to use it with the 
<b>RegisterProtocol</b> function.


### -param pServiceChar [in, out]

On input, pointer to an 
<a href="https://msdn.microsoft.com/92a117ae-3a5f-4702-a936-8e23bc575763">MPR_SERVICE_CHARACTERISTICS</a> structure. 




On output, receives pointers to functions implemented for the routing protocol.

See the reference page for the 
<a href="https://msdn.microsoft.com/92a117ae-3a5f-4702-a936-8e23bc575763">MPR_SERVICE_CHARACTERISTICS</a> structure for more information on how to use it with the 
<b>RegisterProtocol</b> function.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is ERROR_NOT_SUPPORTED.




## -remarks



All routing protocol DLLs must fill in values for the 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a> structure.

Routing protocol DLLs that provide services must fill in values for the 
<a href="https://msdn.microsoft.com/92a117ae-3a5f-4702-a936-8e23bc575763">MPR_SERVICE_CHARACTERISTICS</a> structure. If a routing protocol DLL does not provide services, it should fill in zero for the <b>fSupportedFunctionality</b> member of this structure, but need not fill in values for the other members.

Routing protocols are implemented in user-mode DLLs. A single DLL may implement multiple routing protocols. Therefore, router manager may call 
<b>RegisterProtocol</b> multiple times, once for each routing protocol implemented in the DLL.




## -see-also




<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/92a117ae-3a5f-4702-a936-8e23bc575763">MPR_SERVICE_CHARACTERISTICS</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>
 

 

