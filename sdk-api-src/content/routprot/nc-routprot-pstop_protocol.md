---
UID: NC:routprot.PSTOP_PROTOCOL
title: PSTOP_PROTOCOL (routprot.h)
description: The StopProtocol function causes the routing protocol to perform an orderly shutdown.
helpviewer_keywords: ["PSTOP_PROTOCOL","PSTOP_PROTOCOL callback","StopProtocol","StopProtocol callback function [RAS]","_mpr_stopprotocol","routprot/StopProtocol","rras.stopprotocol"]
old-location: rras\stopprotocol.htm
tech.root: RRAS
ms.assetid: 8b9459f8-152c-4ec1-9ed0-2b27a56f521d
ms.date: 12/05/2018
ms.keywords: PSTOP_PROTOCOL, PSTOP_PROTOCOL callback, StopProtocol, StopProtocol callback function [RAS], _mpr_stopprotocol, routprot/StopProtocol, rras.stopprotocol
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSTOP_PROTOCOL
 - routprot/PSTOP_PROTOCOL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - StopProtocol
---

# PSTOP_PROTOCOL callback function


## -description

The 
<b>StopProtocol</b> function causes the routing protocol to perform an orderly shutdown.

## -parameters

### -param unnamedParam1

## -returns

If the routing protocol shutdown successfully (synchronous completion), the return value is NO_ERROR.

If routing protocol is shutting down asynchronously, the return value is ERROR_PROTOCOL_STOP_PENDING. In this case, the protocol  reports the results of the shutdown through the event message queue.

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pstart_protocol">StartProtocol</a>