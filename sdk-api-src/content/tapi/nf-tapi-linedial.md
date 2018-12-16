---
UID: NF:tapi.lineDial
title: lineDial function
author: windows-sdk-content
description: The lineDial function dials the specified dialable number on the specified call.
old-location: tapi2\linedial.htm
tech.root: tapi
ms.assetid: 111e6c11-67a7-4aab-81dd-f1b4316887e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linedial, lineDial, lineDial function [TAPI 2.2], lineDialA, lineDialW, tapi/lineDial, tapi/lineDialA, tapi/lineDialW, tapi2.linedial"
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineDialW (Unicode) and lineDialA (ANSI)
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
 - lineDial
 - lineDialA
 - lineDialW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineDial function


## -description


The 
<b>lineDial</b> function dials the specified dialable number on the specified call.


## -parameters




### -param hCall

Handle to the call on which a number is to be dialed. The application must be an owner of the call. The call state of <i>hCall</i> can be any state except <i>idle</i> and <i>disconnected</i>.


### -param lpszDestAddress

Destination to be dialed using the standard dialable number format.


### -param dwCountryCode

Country or region code of the destination. This is used by the implementation to select the call progress protocols for the destination address. If a value of 0 is specified, a service provider-defined default call progress protocol is used.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_ADDRESSBLOCKED, LINEERR_INVALPOINTER, LINEERR_DIALBILLING, LINEERR_NOMEM, LINEERR_DIALDIALTONE, LINEERR_NOTOWNER, LINEERR_DIALPROMPT, LINEERR_OPERATIONFAILED, LINEERR_DIALQUIET, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_UNINITIALIZED, LINEERR_INVALCOUNTRYCODE.




## -remarks



If LINEERR_INVALADDRESS is returned, no dialing has been done. If LINEERR_DIALBILLING, LINEERR_DIALQUIET, LINEERR_DIALDIALTONE, or LINEERR_DIALPROMPT is returned, none of the actions otherwise performed by 
<b>lineDial</b> have occurred. For example, none of the dialable addresses prior to the offending character has been dialed, no hookswitch state has changed, and so on.

The 
<b>lineDial</b> function is used for dialing on an existing call appearance. For example, after a call has been set up for transfer or conference, a consultation call is automatically allocated, and the 
<b>lineDial</b> function would be used to perform the dialing of this consultation call. The 
<b>lineDial</b> function can be invoked multiple times in the course of multistage dialing, if the line's device capabilities allow it. Also, multiple addresses can be provided in a single dial string separated by CRLF. Service providers that provide inverse multiplexing can establish individual physical calls with each of the addresses and can return a single call handle to the aggregate of all calls to the application. All addresses would use the same country or region code.

Dialing is considered complete after the address has been passed to the service provider; not after the call is finally connected. Service providers that provide inverse multiplexing can allow multiple addresses to be provided at once. The service provider sends LINE_CALLSTATE messages to the application to inform it about the progress of the call. To abort a call attempt while a call is being established, the invoking application should use 
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>.

An application can set the <i>lpszDestAddress</i> parameter of the 
<b>lineDial</b> function to the address of an empty string to indicate that dialing is complete, but only if the previous calls to the 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> and 
<b>lineDial</b> functions have had the strings specified by <i>lpszDestAddress</i> terminated with semicolons.

The <b>lineDial</b> function can also be used in partial dialing.  To initiate a call using partial dialing, the application calls <a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> and specifies a partial dialing string. A partial dial string is any dial string  terminated by a semicolon.  The call will typically transition to LINECALLSTATE_DIALING after which <b>lineDial</b> can be called to specify  more dialing strings, each terminated by a semicolon.  Dialing is completed by calling <b>lineDial</b> with a dial string that is not terminated with a semicolon (such as an empty string).  This technique allows applications to perform interactive partial dialing with the user  or enable  more sophisticated dialing than a TSP may be capable of.



If a null destination string, or an empty string terminated with a semicolon (";") is entered in   <a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> the application transitions to LINE_CALLSTATE_DIALTONE. The  <b>lineDial</b> function can  be called in this state to enter a single dial string  or  multiple partial dial strings, each separated by a semicolon. The application transitions to the  LINECALLSTATE_DIALING state after the first digit is entered.

<div class="alert"><b>Note</b>  The <b>lineDial</b> function is  only available when a call is in LINECALLSTATE_DIALING or LINE_CALLSTATE_DIALTONE.  If DTMF is needed while a call is connected  (LINECALLSTATE_CONNECTED), use <a href="https://msdn.microsoft.com/aa407269-06be-43e2-906e-20137e4bdb89">lineGenerateDigits</a>.
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/1dfaefd7-f8dd-451e-af18-249c89bdb517">Dial Overview</a>



<a href="../tapi3/address_ovr.htm">Dialable Addresses</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>
 

 

