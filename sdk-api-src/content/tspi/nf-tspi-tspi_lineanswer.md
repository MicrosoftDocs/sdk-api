---
UID: NF:tspi.TSPI_lineAnswer
title: TSPI_lineAnswer function
author: windows-sdk-content
description: The TSPI_lineAnswer function answers the specified offering call.
old-location: tspi\tspi_lineanswer.htm
old-project: tapi
ms.assetid: efd4d7f8-bf81-46c4-b51b-516036e9baef
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TSPI_lineAnswer, TSPI_lineAnswer function [TAPI 2.2], _tspi_tspi_lineanswer, tspi.tspi_lineanswer, tspi/TSPI_lineAnswer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineAnswer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineAnswer function


## -description


The 
<b>TSPI_lineAnswer</b> function answers the specified offering call.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call to be answered. The call state of <i>hdCall</i> can be <i>offering</i> or <i>accepted</i>.


### -param lpsUserUserInfo

A pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party at the time of answering the call. If this pointer is <b>NULL</b>, it indicates that no user-user information is to be sent. User-user information is only sent if supported by the underlying network (as indicated in 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>).


### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INUSE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG.




## -remarks



When a new call arrives, the service provider sends TAPI a 
<a href="https://msdn.microsoft.com/36122dfb-1ed6-459d-aa2b-69c86daaddd8">LINE_NEWCALL</a> message to exchange handles for the call. The service provider follows this with a 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> message to inform TAPI and its client applications of the call's state. A client application typically answers the call using 
<b>TSPI_lineAnswer</b>. Typically, after the call is successfully answered, the call transitions to the <i>connected</i> state.

In some telephony environments (like ISDN) where user alerting is separate from call offering, TAPI and its client applications may have the option to first accept a call prior to answering, or instead to reject or redirect the <i>offering</i> call.

If a call is offered at the time another call is already active, the new call is connected to by invoking 
<b>TSPI_lineAnswer</b>. The effect this has on the existing active call depends on the line's device capabilities. The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold. The appropriate LINE_CALLSTATE messages are used to report state transitions to TAPI about both calls.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/36122dfb-1ed6-459d-aa2b-69c86daaddd8">LINE_NEWCALL</a>
 

 

