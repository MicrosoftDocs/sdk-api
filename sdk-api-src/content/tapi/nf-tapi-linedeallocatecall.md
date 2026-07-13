---
UID: NF:tapi.lineDeallocateCall
title: lineDeallocateCall function (tapi.h)
description: Deallocates the specified call handle.
helpviewer_keywords: ["_tapi2_linedeallocatecall","lineDeallocateCall","lineDeallocateCall function [TAPI 2.2]","tapi/lineDeallocateCall","tapi2.linedeallocatecall"]
old-location: tapi2\linedeallocatecall.htm
tech.root: tapi3
ms.assetid: a695ee19-e371-4126-b438-62bf52179cba
ms.date: 12/05/2018
ms.keywords: _tapi2_linedeallocatecall, lineDeallocateCall, lineDeallocateCall function [TAPI 2.2], tapi/lineDeallocateCall, tapi2.linedeallocatecall
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
 - lineDeallocateCall
 - tapi/lineDeallocateCall
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
 - lineDeallocateCall
---

# lineDeallocateCall function


## -description

The 
<b>lineDeallocateCall</b> function deallocates the specified call handle.

## -parameters

### -param hCall

The call handle to be deallocated. An application with monitoring privileges for a call can always deallocate its handle for that call. An application with owner privilege for a call can deallocate its handle unless it is the sole owner of the call and the call is not in the <i>idle</i> state. The call handle is no longer valid after it has been deallocated.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values include:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

The deallocation does not affect the call state of the physical call. It does, however, release internal resources related to the call.

In API versions, earlier than 2.0, if the application is the sole owner of a call and the call is not in the <i>idle</i> state, LINEERR_INVALCALLSTATE is returned. In this case, the application can first drop the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a> and deallocate its call handle afterward. An application that has monitor privilege for a call can always deallocate its handle for the call.

In API versions 2.0 or later, the sole owner of the call can deallocate its handle even though the call is not in the <i>idle</i> state. This enables distributed control of the call in a client/server environment.

<div class="alert"><b>Note</b>  Leaving the call without an owner can result in the user being unable to terminate the call if there are monitoring applications open preventing TAPI from calling 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosecall">TSPI_lineCloseCall</a>. Use this feature only if the application can determine that the call can be controlled externally by the user. For more information, see LINEADDRCAPFLAGS_CLOSEDROP.</div>
<div> </div>
In API versions earlier than 2.0, when the 
<b>lineDeallocateCall</b> function deallocates a call handle, it also suspends further processing of any outstanding LINE_REPLY messages for the call. An application must be designed not to wait indefinitely for LINE_REPLY messages for each corresponding call to an asynchronous function if it also uses the 
<b>lineDeallocateCall</b> function to deallocate handles.

In API versions 2.0 or later, 
<b>lineDeallocateCall</b> does not suspend outstanding LINE_REPLY messages; every asynchronous function that returns a <i>dwRequestID</i> to the application always results in the delivery of the associated LINE_REPLY message unless the application calls 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/terminate-a-session-ovr">Terminate a Session Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>