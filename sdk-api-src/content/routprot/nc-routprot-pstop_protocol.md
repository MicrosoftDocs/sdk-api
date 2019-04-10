---
UID: NC:routprot.PSTOP_PROTOCOL
title: PSTOP_PROTOCOL (routprot.h)
author: windows-sdk-content
description: The StopProtocol function causes the routing protocol to perform an orderly shutdown.
old-location: rras\stopprotocol.htm
tech.root: RRAS
ms.assetid: 8b9459f8-152c-4ec1-9ed0-2b27a56f521d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSTOP_PROTOCOL, PSTOP_PROTOCOL callback, StopProtocol, StopProtocol callback function [RAS], _mpr_stopprotocol, routprot/StopProtocol, rras.stopprotocol
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
 - StopProtocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSTOP_PROTOCOL callback function


## -description


The 
<b>StopProtocol</b> function causes the routing protocol to perform an orderly shutdown.


## -parameters




### -param Arg1








## -returns



If the routing protocol shutdown successfully (synchronous completion), the return value is NO_ERROR.

If routing protocol is shutting down asynchronously, the return value is ERROR_PROTOCOL_STOP_PENDING. In this case, the protocol  reports the results of the shutdown through the event message queue.




## -see-also




<a href="https://msdn.microsoft.com/59aa7bd8-3510-4ca0-90f1-2667dcb4abf0">GetEventMessage</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/8c1c0173-5abf-4e44-a633-16742fd2a4c0">StartProtocol</a>
 

 

