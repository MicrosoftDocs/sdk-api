---
UID: NF:tapi.lineGetQueueListA
title: lineGetQueueListA function (tapi.h)
description: The lineGetQueueList function returns a list of queues associated with a particular ACD Group. (ANSI)
helpviewer_keywords: ["lineGetQueueListA", "tapi/lineGetQueueListA"]
old-location: tapi2\linegetqueuelist.htm
tech.root: tapi3
ms.assetid: 3921ab24-c9c8-4068-a885-e55759f04076
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetqueuelist, lineGetQueueList, lineGetQueueList function [TAPI 2.2], lineGetQueueListA, lineGetQueueListW, tapi/lineGetQueueList, tapi/lineGetQueueListA, tapi/lineGetQueueListW, tapi2.linegetqueuelist
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetQueueListW (Unicode) and lineGetQueueListA (ANSI)
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
 - lineGetQueueListA
 - tapi/lineGetQueueListA
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
 - lineGetQueueList
 - lineGetQueueListA
 - lineGetQueueListW
---

# lineGetQueueListA function


## -description

The 
<b>lineGetQueueList</b> function returns a list of queues associated with a particular ACD Group. It generates a 
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_GETQUEUELIST.

## -parameters

### -param hLine

Handle to the line device.

### -param lpGroupID

Pointer to GUID that identifies the group for which the list of queues is requested.

### -param lpQueueList

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeuelist">LINEQUEUELIST</a>. Upon successful completion of the request, this structure is filled with a list of queues. Prior to calling 
<b>lineGetQueueList</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linequeuelist">LINEQUEUELIST</a>



<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetQueueList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
