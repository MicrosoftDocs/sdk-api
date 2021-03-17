---
UID: NF:tapi.lineSetAgentSessionState
title: lineSetAgentSessionState function (tapi.h)
description: The lineSetAgentSessionState function sets the agent session state associated with a particular agent session handle.
helpviewer_keywords: ["_tapi2_linesetagentsessionstate","lineSetAgentSessionState","lineSetAgentSessionState function [TAPI 2.2]","tapi/lineSetAgentSessionState","tapi2.linesetagentsessionstate"]
old-location: tapi2\linesetagentsessionstate.htm
tech.root: tapi3
ms.assetid: 284d8411-6ac7-4496-893b-0349057523e8
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetagentsessionstate, lineSetAgentSessionState, lineSetAgentSessionState function [TAPI 2.2], tapi/lineSetAgentSessionState, tapi2.linesetagentsessionstate
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
 - lineSetAgentSessionState
 - tapi/lineSetAgentSessionState
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
 - lineSetAgentSessionState
---

# lineSetAgentSessionState function


## -description

The 
<b>lineSetAgentSessionState</b> function sets the agent session state associated with a particular agent session handle. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTSESSIONSTATE.

## -parameters

### -param hLine

Handle to the line device.

### -param hAgentSession

Identifier of the agent session whose information is to be changed.

### -param dwAgentSessionState

New agent session state. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentsessionstate--constants">LINEAGENTSESSIONSTATE_ constants</a> or zero to leave the agent session state unchanged and modify only the next state.

### -param dwNextAgentSessionState

Next agent session state. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentsessionstate--constants">LINEAGENTSESSIONSTATE_ constants</a> or zero.

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/Tapi/lineagentsessionstate--constants">LINEAGENTSESSIONSTATE_ constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>