---
UID: NF:tapi.lineGetAgentSessionInfo
title: lineGetAgentSessionInfo function (tapi.h)
description: The lineGetAgentSessionInfo function returns a structure that holds the ACD information associated with a particular agent session handle.
helpviewer_keywords: ["_tapi2_linegetagentsessioninfo","lineGetAgentSessionInfo","lineGetAgentSessionInfo function [TAPI 2.2]","tapi/lineGetAgentSessionInfo","tapi2.linegetagentsessioninfo"]
old-location: tapi2\linegetagentsessioninfo.htm
tech.root: tapi3
ms.assetid: 06a5ea23-4205-46fd-abe7-ee4575be81c8
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetagentsessioninfo, lineGetAgentSessionInfo, lineGetAgentSessionInfo function [TAPI 2.2], tapi/lineGetAgentSessionInfo, tapi2.linegetagentsessioninfo
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
 - lineGetAgentSessionInfo
 - tapi/lineGetAgentSessionInfo
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
 - lineGetAgentSessionInfo
---

# lineGetAgentSessionInfo function


## -description

The 
<b>lineGetAgentSessionInfo</b> function returns a structure that holds the ACD information associated with a particular agent session handle. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTSESSIONINFO.

## -parameters

### -param hLine

Handle to the line device.

### -param hAgentSession

Identifier of the agent session whose information is to be retrieved.

### -param lpAgentSessionInfo

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessioninfo">LINEAGENTSESSIONINFO</a>. Upon successful completion of the request, this structure is filled with the agent session statistics. Prior to calling the 
<b>lineGetAgentSessionInfo</b> function, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that memory could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagentsessioninfo">LINEAGENTSESSIONINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>