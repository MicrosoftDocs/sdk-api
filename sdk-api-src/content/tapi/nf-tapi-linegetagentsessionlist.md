---
UID: NF:tapi.lineGetAgentSessionList
title: lineGetAgentSessionList function (tapi.h)
description: The lineGetAgentSessionList function returns a list of agent sessions created for the specified agent.
helpviewer_keywords: ["_tapi2_linegetagentsessionlist","lineGetAgentSessionList","lineGetAgentSessionList function [TAPI 2.2]","tapi/lineGetAgentSessionList","tapi2.linegetagentsessionlist"]
old-location: tapi2\linegetagentsessionlist.htm
tech.root: tapi3
ms.assetid: 6473d5dd-e08e-47f8-acad-b60943525b83
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetagentsessionlist, lineGetAgentSessionList, lineGetAgentSessionList function [TAPI 2.2], tapi/lineGetAgentSessionList, tapi2.linegetagentsessionlist
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
 - lineGetAgentSessionList
 - tapi/lineGetAgentSessionList
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
 - lineGetAgentSessionList
---

# lineGetAgentSessionList function


## -description

The 
<b>lineGetAgentSessionList</b> function returns a list of agent sessions created for the specified agent. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTSESSIONLIST.

## -parameters

### -param hLine

Handle to the line device.

### -param hAgent

Identifier of the agent whose information is to be retrieved.

### -param lpAgentSessionList

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist">LINEAGENTSESSIONLIST</a>. Upon successful completion of the request, this structure is filled with a list of the agent sessions that have been created for this agent. Prior to calling the 
<b>lineGetAgentSessionList</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist">LINEAGENTSESSIONLIST</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>