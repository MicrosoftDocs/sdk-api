---
UID: NF:tapi.lineDeallocateCall
title: lineDeallocateCall function
author: windows-sdk-content
description: Deallocates the specified call handle.
old-location: tapi2\linedeallocatecall.htm
tech.root: tapi
ms.assetid: a695ee19-e371-4126-b438-62bf52179cba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linedeallocatecall, lineDeallocateCall, lineDeallocateCall function [TAPI 2.2], tapi/lineDeallocateCall, tapi2.linedeallocatecall"
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
 - lineDeallocateCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a> and deallocate its call handle afterward. An application that has monitor privilege for a call can always deallocate its handle for the call.

In API versions 2.0 or later, the sole owner of the call can deallocate its handle even though the call is not in the <i>idle</i> state. This enables distributed control of the call in a client/server environment.

<div class="alert"><b>Note</b>  Leaving the call without an owner can result in the user being unable to terminate the call if there are monitoring applications open preventing TAPI from calling 
<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>. Use this feature only if the application can determine that the call can be controlled externally by the user. For more information, see LINEADDRCAPFLAGS_CLOSEDROP.</div>
<div> </div>
In API versions earlier than 2.0, when the 
<b>lineDeallocateCall</b> function deallocates a call handle, it also suspends further processing of any outstanding LINE_REPLY messages for the call. An application must be designed not to wait indefinitely for LINE_REPLY messages for each corresponding call to an asynchronous function if it also uses the 
<b>lineDeallocateCall</b> function to deallocate handles.

In API versions 2.0 or later, 
<b>lineDeallocateCall</b> does not suspend outstanding LINE_REPLY messages; every asynchronous function that returns a <i>dwRequestID</i> to the application always results in the delivery of the associated LINE_REPLY message unless the application calls 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d">Terminate a Session Overview</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>



<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>
 

 

