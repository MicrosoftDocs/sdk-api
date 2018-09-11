---
UID: NF:tapi.lineCompleteCall
title: lineCompleteCall function
author: windows-sdk-content
description: The lineCompleteCall function specifies how a call that could not be connected normally should be completed instead.
old-location: tapi2\linecompletecall.htm
tech.root: tapi
ms.assetid: 4cc4c1fd-3f54-40ec-9342-58b3783031ad
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linecompletecall, lineCompleteCall, lineCompleteCall function [TAPI 2.2], tapi/lineCompleteCall, tapi2.linecompletecall"
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
 - lineCompleteCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineCompleteCall function


## -description


The 
<b>lineCompleteCall</b> function specifies how a call that could not be connected normally should be completed instead. The network or switch may not be able to complete a call because network resources are busy or the remote station is busy or doesn't answer. The application can request that the call be completed in one of a number of ways.


## -parameters




### -param hCall

Handle to the call whose completion is requested. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>busy</i> or <i>ringback</i>.


### -param lpdwCompletionID

Pointer to a <b>DWORD</b>-sized memory location. The completion identifier is used to identify individual completion requests in progress. A completion identifier becomes invalid and can be reused after the request completes or after an outstanding request is canceled.


### -param dwCompletionMode

Way in which the call is to be completed. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/68f755a1-586b-4c5b-b8e8-c8b40eb71685">LINECALLCOMPLMODE_ Constants</a>.


### -param dwMessageID

Message that is to be sent when completing the call using LINECALLCOMPLMODE_MESSAGE. This identifier selects the message from a small number of predefined messages.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_COMPLETIONOVERRUN, LINEERR_NOMEM, LINEERR_INVALCALLCOMPLMODE, LINEERR_NOTOWNER, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALMESSAGEID, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED.




## -remarks



This function is considered complete when the request has been accepted by the network or switch; not when the request is fully completed in the way specified. After this function completes, the call typically transitions to <i>idle</i>. When the called station or network enters a state where the call can be completed as requested, the application is notified by a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message with the call state equal to <i>offering</i>. The call's 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> record lists the reason for the call as CALLCOMPLETION and provides the completion identifier as well. It is possible to have multiple outstanding call completion requests; the maximum number is device dependent. The completion identifier is also used to refer to each individual request so requests can be canceled by calling 
<a href="https://msdn.microsoft.com/e6b87d84-071c-4b75-afbf-569a5a861e3a">lineUncompleteCall</a>.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e6b87d84-071c-4b75-afbf-569a5a861e3a">lineUncompleteCall</a>
 

 

