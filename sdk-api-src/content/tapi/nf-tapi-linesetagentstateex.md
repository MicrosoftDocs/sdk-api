---
UID: NF:tapi.lineSetAgentStateEx
title: lineSetAgentStateEx function (tapi.h)
description: The lineSetAgentStateEx function sets the agent state associated with a particular agent handle.
helpviewer_keywords: ["_tapi2_linesetagentstateex","lineSetAgentStateEx","lineSetAgentStateEx function [TAPI 2.2]","tapi/lineSetAgentStateEx","tapi2.linesetagentstateex"]
old-location: tapi2\linesetagentstateex.htm
tech.root: tapi3
ms.assetid: f7da697a-658e-4f0d-8e6c-539fd8fb1935
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetagentstateex, lineSetAgentStateEx, lineSetAgentStateEx function [TAPI 2.2], tapi/lineSetAgentStateEx, tapi2.linesetagentstateex
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetAgentStateEx
 - tapi/lineSetAgentStateEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetAgentStateEx
---

# lineSetAgentStateEx function


## -description

The 
<b>lineSetAgentStateEx</b> function sets the agent state associated with a particular agent handle. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTSTATEEX.

## -parameters

### -param hLine

Handle to the line device.

### -param hAgent

Identifier of the agent whose information is to be changed.

### -param dwAgentState

New agent state. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstateex--constants">LINEAGENTSTATEEX_ constants</a>, or zero to leave the agent state unchanged and modify only the next state.

### -param dwNextAgentState

Next agent state. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstateex--constants">LINEAGENTSTATEEX_ constants</a> or zero.

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>