---
UID: NF:tspi.TSPI_lineSendUserUserInfo
title: TSPI_lineSendUserUserInfo function
author: windows-sdk-content
description: The TSPI_lineSendUserUserInfo function sends user-user information to the remote party on the specified call.
old-location: tspi\tspi_linesenduseruserinfo.htm
tech.root: tapi
ms.assetid: a63fcb64-f509-4cc0-a388-91f7e05e2ef0
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: TSPI_lineSendUserUserInfo, TSPI_lineSendUserUserInfo function [TAPI 2.2], _tspi_tspi_linesenduseruserinfo, tspi.tspi_linesenduseruserinfo, tspi/TSPI_lineSendUserUserInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>).


### -param dwSize

The size, in bytes, including the <b>null</b> terminator, of the user-user information in <i>lpsUserUserInfo</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.




## -remarks



This function can be used to send user-user information at any time during a connected call. If the size of the specified information to be sent is larger than what can fit into a single network message (as in ISDN), the service provider is responsible for breaking the information up into a sequence of chained network messages (using "more data").

User-user information can also be sent as part of call accept, call reject, call redirect, and when making calls. User-user information can also be received. The received information is reported in the call's 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure. Whenever user-user information arrives after call offering or prior to call disconnect, a 
<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a> message with a <i>UserUserInfo</i> parameter notifies TAPI that user-user information in the call-information record has changed. If multiple network messages are chained, the information is assembled by the service provider and a single message is sent to TAPI.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/2690992b-b155-4ae9-816a-e5fafaffa033">TSPI_lineAccept</a>



<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/9c3d6a7d-b0bf-4068-9d64-e0c715a8c011">TSPI_lineMakeCall</a>



<a href="https://msdn.microsoft.com/835fce4a-69c4-4a7e-846f-f05df4a24b96">TSPI_lineRedirect</a>
 

 

