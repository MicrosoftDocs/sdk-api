---
UID: NC:routprot.PREGISTER_PROTOCOL
title: PREGISTER_PROTOCOL (routprot.h)
description: The RegisterProtocol function registers the routing protocol with the router manager. It also informs the router manager of the functionality that the routing protocol supports.
helpviewer_keywords: ["PREGISTER_PROTOCOL","PREGISTER_PROTOCOL callback","RegisterProtocol","RegisterProtocol callback function [RAS]","_mpr_registerprotocol","routprot/RegisterProtocol","rras.registerprotocol"]
old-location: rras\registerprotocol.htm
tech.root: RRAS
ms.assetid: b9027ef9-e573-4df0-b37e-d09956c1f8ee
ms.date: 12/05/2018
ms.keywords: PREGISTER_PROTOCOL, PREGISTER_PROTOCOL callback, RegisterProtocol, RegisterProtocol callback function [RAS], _mpr_registerprotocol, routprot/RegisterProtocol, rras.registerprotocol
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
 - PREGISTER_PROTOCOL
 - routprot/PREGISTER_PROTOCOL
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
 - RegisterProtocol
---

# PREGISTER_PROTOCOL callback function


## -description

The 
<b>RegisterProtocol</b> function registers the routing protocol with the router manager. It also informs the router manager of the functionality that the routing protocol supports.

## -parameters

### -param pRoutingChar [in, out]

On input, pointer to an 
<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a> structure. 




On output, receives pointers to functions implemented for the routing protocol.

See the reference page for the 
<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a> structure for more information on how to use it with the 
<b>RegisterProtocol</b> function.

### -param pServiceChar [in, out]

On input, pointer to an 
<a href="/windows/desktop/api/stm/ns-stm-mpr40_service_characteristics">MPR_SERVICE_CHARACTERISTICS</a> structure. 




On output, receives pointers to functions implemented for the routing protocol.

See the reference page for the 
<a href="/windows/desktop/api/stm/ns-stm-mpr40_service_characteristics">MPR_SERVICE_CHARACTERISTICS</a> structure for more information on how to use it with the 
<b>RegisterProtocol</b> function.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is ERROR_NOT_SUPPORTED.

## -remarks

All routing protocol DLLs must fill in values for the 
<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a> structure.

Routing protocol DLLs that provide services must fill in values for the 
<a href="/windows/desktop/api/stm/ns-stm-mpr40_service_characteristics">MPR_SERVICE_CHARACTERISTICS</a> structure. If a routing protocol DLL does not provide services, it should fill in zero for the <b>fSupportedFunctionality</b> member of this structure, but need not fill in values for the other members.

Routing protocols are implemented in user-mode DLLs. A single DLL may implement multiple routing protocols. Therefore, router manager may call 
<b>RegisterProtocol</b> multiple times, once for each routing protocol implemented in the DLL.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a>



<a href="/windows/desktop/api/stm/ns-stm-mpr40_service_characteristics">MPR_SERVICE_CHARACTERISTICS</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>