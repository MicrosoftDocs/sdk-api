---
UID: NF:tapi.lineSetAgentStateEx
title: lineSetAgentStateEx function (tapi.h)
author: windows-sdk-content
description: The lineSetAgentStateEx function sets the agent state associated with a particular agent handle.
old-location: tapi2\linesetagentstateex.htm
tech.root: Tapi
ms.assetid: f7da697a-658e-4f0d-8e6c-539fd8fb1935
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linesetagentstateex, lineSetAgentStateEx, lineSetAgentStateEx function [TAPI 2.2], tapi/lineSetAgentStateEx, tapi2.linesetagentstateex"
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
 - lineSetAgentStateEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetAgentStateEx function


## -description


The 
<b>lineSetAgentStateEx</b> function sets the agent state associated with a particular agent handle. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTSTATEEX.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgent

Identifier of the agent whose information is to be changed.


### -param dwAgentState

New agent state. Must be one of the 
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ constants</a>, or zero to leave the agent state unchanged and modify only the next state.


### -param dwNextAgentState

Next agent state. Must be one of the 
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ constants</a> or zero.


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALAGENTSTATE, LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

