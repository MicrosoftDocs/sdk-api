---
UID: NF:tspi.TSPI_lineAccept
title: TSPI_lineAccept function
author: windows-sdk-content
description: The TSPI_lineAccept function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.
old-location: tspi\tspi_lineaccept.htm
tech.root: TAPI
ms.assetid: 2690992b-b155-4ae9-816a-e5fafaffa033
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_lineAccept, TSPI_lineAccept function [TAPI 2.2], _tspi_tspi_lineaccept, tspi.tspi_lineaccept, tspi/TSPI_lineAccept
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
 - TSPI_lineAccept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineAccept function


## -description


The 
<b>TSPI_lineAccept</b> function accepts the specified offered call. It can optionally send the specified user-user information to the calling party.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call to be accepted. The call state of <i>hdCall</i> can be <i>offering</i>.


### -param lpsUserUserInfo

A pointer to a <b>null</b>-terminated Unicode string containing user-user information to be sent to the remote party as part of the call accept. This pointer is <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>).


### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.


## -returns



Returns <i>dwRequestID</i> if the function is completed asynchronously or an error number if an error occurs. The <i>lResult</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.




## -remarks



The 
<b>TSPI_lineAccept</b> function is used in telephony environments (such as ISDN) that allow alerting associated with incoming calls to be separate from the initial offering of the call. When a call comes in, the call is first offered. For some small time duration, the client application may have the option to reject the call using 
<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>, redirect the call to another station using 
<a href="https://msdn.microsoft.com/835fce4a-69c4-4a7e-846f-f05df4a24b96">TSPI_lineRedirect</a>, answer the call using 
<a href="https://msdn.microsoft.com/efd4d7f8-bf81-46c4-b51b-516036e9baef">TSPI_lineAnswer</a>, or accept the call using 
<b>TSPI_lineAccept</b>. After a call has been successfully accepted, alerting at both the called and calling device begins, and typically the call state transitions to the <i>accepted</i> state. The service provider must set the flag LINEADDRCAPFLAGS_ACCEPTTOALERT in the <b>dwAddrCapFlags</b> member of the 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> data structure if the application must call 
<b>TSPI_lineAccept</b> for alerting to begin.

To TAPI, alerting is reported using the 
<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a> message with the <i>ringing</i> indication.

<b>TSPI_lineAccept</b> may also be supported by non-ISDN service providers. The call state transition to the <i>accepted</i> state can be used by other of the TAPI clients as an indication that some application has claimed responsibility for the call and has presented the call to the user.

The client application has the option to send user-user information at the time of the accept. Even if user-user information can be sent, often no guarantees are made that the network will deliver this information to the calling party. The client application may consult a line's device capabilities to determine whether call accept is available.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/efd4d7f8-bf81-46c4-b51b-516036e9baef">TSPI_lineAnswer</a>



<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>



<a href="https://msdn.microsoft.com/97cde843-65bc-46ae-a6ae-724f2c9c5217">TSPI_lineOpen</a>



<a href="https://msdn.microsoft.com/835fce4a-69c4-4a7e-846f-f05df4a24b96">TSPI_lineRedirect</a>
 

 

