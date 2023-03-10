---
UID: NF:tapi.lineGetQueueInfo
title: lineGetQueueInfo function (tapi.h)
description: The lineGetQueueInfo function returns a structure holding the ACD information associated with a particular queue.
helpviewer_keywords: ["_tapi2_linegetqueueinfo","lineGetQueueInfo","lineGetQueueInfo function [TAPI 2.2]","tapi/lineGetQueueInfo","tapi2.linegetqueueinfo"]
old-location: tapi2\linegetqueueinfo.htm
tech.root: tapi3
ms.assetid: f7bd6922-a9cd-43ab-96f7-5abf4c6a5b16
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetqueueinfo, lineGetQueueInfo, lineGetQueueInfo function [TAPI 2.2], tapi/lineGetQueueInfo, tapi2.linegetqueueinfo
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
 - lineGetQueueInfo
 - tapi/lineGetQueueInfo
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
 - lineGetQueueInfo
---

# lineGetQueueInfo function


## -description

The 
<b>lineGetQueueInfo</b> function returns a structure holding the ACD information associated with a particular queue. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETQUEUEINFO.

## -parameters

### -param hLine

Handle to the line device.

### -param dwQueueID

Identifier of the queue whose information is to be retrieved.

### -param lpLineQueueInfo

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeueinfo">LINEQUEUEINFO</a>. Upon successful completion of the request, this structure is filled with the queue statistics. Prior to calling 
<b>lineGetQueueInfo</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linequeueinfo">LINEQUEUEINFO</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>