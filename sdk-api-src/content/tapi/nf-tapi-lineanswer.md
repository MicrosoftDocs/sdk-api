---
UID: NF:tapi.lineAnswer
title: lineAnswer function
author: windows-sdk-content
description: The lineAnswer function answers the specified offering call.
old-location: tapi2\lineanswer.htm
tech.root: tapi
ms.assetid: dd51991c-c044-4b88-8f97-9e0ae701a2a5
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_lineanswer, lineAnswer, lineAnswer function [TAPI 2.2], tapi/lineAnswer, tapi2.lineanswer"
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
 - lineAnswer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineAnswer function


## -description


The 
<b>lineAnswer</b> function answers the specified offering call.


## -parameters




### -param hCall

Handle to the call to be answered. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>offering</i> or <i>accepted</i>.


### -param lpsUserUserInfo

Pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party at the time the call is answered. This pointer can be left <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>). The protocol discriminator field for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>. 


### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i> (including the <b>null</b> terminator), in bytes If <i>lpsUserUserInfo</i> is <b>NULL</b>, no user-user information is sent to the calling party and <i>dwSize</i> is ignored. 


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INUSE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_NOTOWNER.




## -remarks



When a new call arrives, applications with an interest in the call are sent a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message to provide the new call handle and to inform the application about the call's state and the privileges to the new call (such as monitor or owner). The application with owner privilege for the call can answer this call using 
<b>lineAnswer</b>. After the call has been successfully answered, the call typically transitions to the <i>connected</i> state. Initially, only one application is given owner privilege to the incoming call.

In some telephony environments (like ISDN), where user alerting is separate from call offering, the application can have the option to accept a call prior to answering or to reject or redirect the offering call.

If a call comes in (is offered) at the time another call is already active, invoking 
<b>lineAnswer</b> connects to the new call. The effect this has on the existing active call depends on the line's device capabilities. The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold. The appropriate LINE_CALLSTATE messages report state transitions to the application about both calls.

In a bridged situation, if a call is connected but in the LINECONNECTEDMODE_INACTIVE state, it can be joined using the 
<b>lineAnswer</b> function.

The application has the option to send user-user information at the time of the answer. Even if user-user information can be sent, there is no guarantee that the network will deliver this information to the calling party. An application should consult a line's device capabilities to determine whether sending user-user information upon answering the call is available.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

