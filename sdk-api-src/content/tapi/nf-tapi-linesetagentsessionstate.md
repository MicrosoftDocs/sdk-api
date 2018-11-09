---
UID: NF:tapi.lineSetAgentSessionState
title: lineSetAgentSessionState function
author: windows-sdk-content
description: The lineSetAgentSessionState function sets the agent session state associated with a particular agent session handle.
old-location: tapi2\linesetagentsessionstate.htm
tech.root: tapi
ms.assetid: 284d8411-6ac7-4496-893b-0349057523e8
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_tapi2_linesetagentsessionstate, lineSetAgentSessionState, lineSetAgentSessionState function [TAPI 2.2], tapi/lineSetAgentSessionState, tapi2.linesetagentsessionstate"
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
 - lineSetAgentSessionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetAgentSessionState function


## -description


The 
<b>lineSetAgentSessionState</b> function sets the agent session state associated with a particular agent session handle. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTSESSIONSTATE.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgentSession

Identifier of the agent session whose information is to be changed.


### -param dwAgentSessionState

New agent session state. Must be one of the 
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a> or zero to leave the agent session state unchanged and modify only the next state.


### -param dwNextAgentSessionState

Next agent session state. Must be one of the 
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a> or zero.


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

