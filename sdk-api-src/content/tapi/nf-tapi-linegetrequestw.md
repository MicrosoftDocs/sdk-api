---
UID: NF:tapi.lineGetRequestW
title: lineGetRequestW function
author: windows-sdk-content
description: Retrieves the next by-proxy request for the specified request mode.
old-location: tapi2\linegetrequest.htm
old-project: Tapi
ms.assetid: c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linegetrequest, lineGetRequest, lineGetRequest function [TAPI 2.2], lineGetRequestA, lineGetRequestW, tapi/lineGetRequest, tapi/lineGetRequestA, tapi/lineGetRequestW, tapi2.linegetrequest"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetRequestW (Unicode) and lineGetRequestA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineGetRequest
-	lineGetRequestA
-	lineGetRequestW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetRequestW function


## -description


The 
<b>lineGetRequest</b> function retrieves the next by-proxy request for the specified request mode.


## -parameters




### -param hLineApp

The application usage handle for the line portion of TAPI.


### -param dwRequestMode

A type of request to be obtained. Be aware that <i>dwRequestMode</i> can only have one bit set. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/23321700-64d3-45e3-929a-8f5df64dc4be">LINEREQUESTMODE_ Constants</a>.


### -param lpRequestBuffer

A pointer to a memory buffer where the parameters of the request are to be placed. The size of the buffer and the interpretation of the data placed in the buffer depends on the request mode. The application-allocated buffer is assumed to be of sufficient size to hold the request.

If <i>dwRequestMode</i> is LINEREQUESTMODE_MAKECALL, interpret the content of the request buffer using the 
<a href="https://msdn.microsoft.com/de4e51af-ea1c-41aa-b5a9-9fa628e18d9d">LINEREQMAKECALL</a> structure.

LINEREQUESTMODE_MEDIACALL is obsolete.  For more information, see tapiRequestMediaCall.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

<b>LINEERR_INVALAPPHANDLE</b>, <b>LINEERR_NOTREGISTERED</b>, <b>LINEERR_INVALPOINTER</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINEERR_INVALREQUESTMODE</b>, <b>LINEERR_RESOURCEUNAVAIL</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_UNINITIALIZED</b>, <b>LINEERR_NOREQUEST</b>.




## -remarks



A telephony-enabled application can request that a call be placed on its behalf by invoking 
<a href="https://msdn.microsoft.com/bdbc1565-6570-4fad-890c-fb3965cce452">tapiRequestMakeCall</a>. These requests are queued by TAPI and the highest priority application that has registered to handle the request is sent a 
<a href="https://msdn.microsoft.com/d4dbba0d-8225-48d7-a66b-b189fdae70a8">LINE_REQUEST</a> message with indication of the mode of the request that is pending. Typically, this application is the user's call-control application. The LINE_REQUEST message indicates that zero or more requests may be pending for the registered application to process; after receiving LINE_REQUEST, it is the responsibility of the recipient application to call 
<b>lineGetRequest</b> until LINEERR_NOREQUEST is returned, indicating that no more requests are pending.

Next, the call-control application that receives this message invokes 
<b>lineGetRequest</b>, specifying the request mode and a buffer that is large enough to hold the request. The call-control application then interprets and executes the request.

After execution of 
<b>lineGetRequest</b>, TAPI purges the request from its internal queue, making room available for a subsequent request. It is therefore possible for a new 
<a href="https://msdn.microsoft.com/d4dbba0d-8225-48d7-a66b-b189fdae70a8">LINE_REQUEST</a> message to be received immediately upon execution of 
<b>lineGetRequest</b>, should the same or another application issue another request. It is the responsibility of the request recipient application to handle this scenario by some mechanism; for example, by noting the additional LINE_REQUEST and deferring a subsequent 
<b>lineGetRequest</b> until processing of the preceding request completes, by getting the subsequent request and buffer as necessary, or by another appropriate means.

The subsequent LINE_REQUEST should not be ignored because it is not repeated by TAPI.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/de4e51af-ea1c-41aa-b5a9-9fa628e18d9d">LINEREQMAKECALL</a>



<a href="https://msdn.microsoft.com/d4dbba0d-8225-48d7-a66b-b189fdae70a8">LINE_REQUEST</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/bdbc1565-6570-4fad-890c-fb3965cce452">tapiRequestMakeCall</a>
 

 

