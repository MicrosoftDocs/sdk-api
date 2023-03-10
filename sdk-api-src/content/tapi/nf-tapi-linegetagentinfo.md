---
UID: NF:tapi.lineGetAgentInfo
title: lineGetAgentInfo function (tapi.h)
description: The lineGetAgentInfo function returns a structure holding the ACD information associated with a particular agent handle.
helpviewer_keywords: ["_tapi2_linegetagentinfo","lineGetAgentInfo","lineGetAgentInfo function [TAPI 2.2]","tapi/lineGetAgentInfo","tapi2.linegetagentinfo"]
old-location: tapi2\linegetagentinfo.htm
tech.root: tapi3
ms.assetid: 166b0595-2df0-431f-924c-6899b47408ac
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetagentinfo, lineGetAgentInfo, lineGetAgentInfo function [TAPI 2.2], tapi/lineGetAgentInfo, tapi2.linegetagentinfo
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
 - lineGetAgentInfo
 - tapi/lineGetAgentInfo
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
 - lineGetAgentInfo
---

# lineGetAgentInfo function


## -description

The 
<b>lineGetAgentInfo</b> function returns a structure holding the ACD information associated with a particular agent handle. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETAGENTINFO.

## -parameters

### -param hLine

Handle to the line device.

### -param hAgent

Identifier of the agent whose information is to be retrieved.

### -param lpAgentInfo

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentinfo">LINEAGENTINFO</a>. If the request succeeds, this structure is filled with the agent statistics.

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -remarks

Prior to calling the 
<b>lineGetAgentInfo</b> function, the application should set the <b>dwTotalSize</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentinfo">LINEAGENTINFO</a> structure to indicate the amount of memory available to TAPI for returning information.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagentinfo">LINEAGENTINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>