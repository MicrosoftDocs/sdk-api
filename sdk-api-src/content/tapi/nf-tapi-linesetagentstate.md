---
UID: NF:tapi.lineSetAgentState
title: lineSetAgentState function (tapi.h)
description: The lineSetAgentState function sets the agent state associated with a particular address.
helpviewer_keywords: ["_tapi2_linesetagentstate","lineSetAgentState","lineSetAgentState function [TAPI 2.2]","tapi/lineSetAgentState","tapi2.linesetagentstate"]
old-location: tapi2\linesetagentstate.htm
tech.root: tapi3
ms.assetid: 985798fd-54b1-4674-a1fe-b72c56c5176b
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetagentstate, lineSetAgentState, lineSetAgentState function [TAPI 2.2], tapi/lineSetAgentState, tapi2.linesetagentstate
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
 - lineSetAgentState
 - tapi/lineSetAgentState
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
 - lineSetAgentState
---

# lineSetAgentState function


## -description

The 
<b>lineSetAgentState</b> function sets the agent state associated with a particular address.

## -parameters

### -param hLine

Handle to the line device.

### -param dwAddressID

Identifier of the address for which the agent information is to be changed. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param dwAgentState

New agent state. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ Constants</a>, or zero to leave the agent state unchanged and modify only the next state.

### -param dwNextAgentState

The agent state that should be automatically set when the current call on the address becomes <i>idle</i>. For example, if it is known that after-call work must be performed, this field can be set to LINEAGENTSTATE_WORKAFTERCALL so that a new call is not assigned to the agent after the current call. Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ Constants</a>, or zero to use the default next state configured for the agent.

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALADDRESSSTATE, LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>