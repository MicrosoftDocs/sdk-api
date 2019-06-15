---
UID: NF:tspi.TSPI_lineSendUserUserInfo
title: TSPI_lineSendUserUserInfo function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineSendUserUserInfo function sends user-user information to the remote party on the specified call.
old-location: tspi\tspi_linesenduseruserinfo.htm
tech.root: Tapi
ms.assetid: a63fcb64-f509-4cc0-a388-91f7e05e2ef0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_lineSendUserUserInfo, TSPI_lineSendUserUserInfo function [TAPI 2.2], _tspi_tspi_linesenduseruserinfo, tspi.tspi_linesenduseruserinfo, tspi/TSPI_lineSendUserUserInfo
ms.topic: function
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSendUserUserInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_lineSendUserUserInfo function


## -description


The 
<b>TSPI_lineSendUserUserInfo</b> function sends user-user information to the remote party on the specified call.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call on which to send user-user information. The call state of <i>hdCall</i> can be <i>connected</i>, <i>offering</i>, <i>accepted</i>, or <i>ringback</i>.


### -param lpsUserUserInfo

A pointer to a <b>null</b>-terminated Unicode string containing user-user information to be sent to the remote party. User-user information is only sent if supported by the underlying network (see 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linedevcaps_tag">LINEDEVCAPS</a>).


### -param dwSize

The size, in bytes, including the <b>null</b> terminator, of the user-user information in <i>lpsUserUserInfo</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.




## -remarks



This function can be used to send user-user information at any time during a connected call. If the size of the specified information to be sent is larger than what can fit into a single network message (as in ISDN), the service provider is responsible for breaking the information up into a sequence of chained network messages (using "more data").

User-user information can also be sent as part of call accept, call reject, call redirect, and when making calls. User-user information can also be received. The received information is reported in the call's 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallinfo_tag">LINECALLINFO</a> structure. Whenever user-user information arrives after call offering or prior to call disconnect, a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a> message with a <i>UserUserInfo</i> parameter notifies TAPI that user-user information in the call-information record has changed. If multiple network messages are chained, the information is assembled by the service provider and a single message is sent to TAPI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallinfo_tag">LINECALLINFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_lineaccept">TSPI_lineAccept</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_lineredirect">TSPI_lineRedirect</a>
 

 

