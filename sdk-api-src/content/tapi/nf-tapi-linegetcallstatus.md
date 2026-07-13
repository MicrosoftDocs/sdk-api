---
UID: NF:tapi.lineGetCallStatus
title: lineGetCallStatus function (tapi.h)
description: The lineGetCallStatus function returns the current status of the specified call.
helpviewer_keywords: ["_tapi2_linegetcallstatus","lineGetCallStatus","lineGetCallStatus function [TAPI 2.2]","tapi/lineGetCallStatus","tapi2.linegetcallstatus"]
old-location: tapi2\linegetcallstatus.htm
tech.root: tapi3
ms.assetid: 88bcd211-0993-4703-b43f-4e0b93e3eb7e
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetcallstatus, lineGetCallStatus, lineGetCallStatus function [TAPI 2.2], tapi/lineGetCallStatus, tapi2.linegetcallstatus
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
 - lineGetCallStatus
 - tapi/lineGetCallStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineGetCallStatus
---

# lineGetCallStatus function


## -description

The 
<b>lineGetCallStatus</b> function returns the current status of the specified call.

## -parameters

### -param hCall

Handle to the call to be queried. The call state of <i>hCall</i> can be any state.

### -param lpCallStatus

Pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>. Upon successful completion of the request, this structure is filled with call status information. Prior to calling 
<b>lineGetCallStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL.

## -remarks

The 
<b>lineGetCallStatus</b> function returns the dynamic status of a call, whereas 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a> returns primarily static information about a call. Call status information includes the current call state, detailed mode information related to the call while in this state (if any), as well as a list of the available API functions the application can invoke on the call while the call is in this state. An application would typically be interested in requesting this information when it receives notification about a call state change by the LINE_CALLSTATE message.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>