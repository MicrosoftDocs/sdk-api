---
UID: NF:tapi.lineSetAgentState
title: lineSetAgentState function
author: windows-sdk-content
description: The lineSetAgentState function sets the agent state associated with a particular address.
old-location: tapi2\linesetagentstate.htm
tech.root: tapi
ms.assetid: 985798fd-54b1-4674-a1fe-b72c56c5176b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_linesetagentstate, lineSetAgentState, lineSetAgentState function [TAPI 2.2], tapi/lineSetAgentState, tapi2.linesetagentstate"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetAgentState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ Constants</a>, or zero to leave the agent state unchanged and modify only the next state.


### -param dwNextAgentState

The agent state that should be automatically set when the current call on the address becomes <i>idle</i>. For example, if it is known that after-call work must be performed, this field can be set to LINEAGENTSTATE_WORKAFTERCALL so that a new call is not assigned to the agent after the current call. Must be one of the 
<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ Constants</a>, or zero to use the default next state configured for the agent.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_INVALADDRESSSTATE, LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

