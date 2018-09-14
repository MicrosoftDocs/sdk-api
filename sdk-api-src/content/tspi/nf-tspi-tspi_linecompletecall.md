---
UID: NF:tspi.TSPI_lineCompleteCall
title: TSPI_lineCompleteCall function
author: windows-sdk-content
description: The TSPI_lineCompleteCall function is used to specify how a call that cannot be connected normally is to be completed instead.
old-location: tspi\tspi_linecompletecall.htm
tech.root: TAPI
ms.assetid: ec7b9aec-01f2-497a-924b-471fbb526bee
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_lineCompleteCall, TSPI_lineCompleteCall function [TAPI 2.2], _tspi_tspi_linecompletecall, tspi.tspi_linecompletecall, tspi/TSPI_lineCompleteCall
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
 - TSPI_lineCompleteCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineCompleteCall function


## -description


The 
<b>TSPI_lineCompleteCall</b> function is used to specify how a call that cannot be connected normally is to be completed instead. The network or switch may not be able to complete a call because network resources are busy or the remote station is busy or doesn't answer.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call whose completion is requested. The call state of <i>hdCall</i> can be <i>busy</i>, <i>ringback</i>, or <i>proceeding</i>.


### -param lpdwCompletionID

A pointer to a <b>DWORD</b>-sized memory location where the service provider writes a completion identifier. This uniquely identifies a completion request in progress on the line that contains the <i>hdCall</i>. In particular, a completion identifier becomes invalid after the request completes or is canceled using the 
<a href="https://msdn.microsoft.com/e8b5ee74-245f-4d91-8996-eec482241e4d">TSPI_lineUncompleteCall</a> function. The service provider is free to reuse the completion identifier as soon as it becomes invalid.


### -param dwCompletionMode

The way in which the call is to be completed. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/68f755a1-586b-4c5b-b8e8-c8b40eb71685">LINECALLCOMPLMODE_ constants</a>.


### -param dwMessageID

The message that is to be sent when completing the call using LINECALLCOMPLMODE_MESSAGE. This identifier selects the message from a small number of predefined messages. This parameter is not validated by TAPI when this function is called.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLCOMPLMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_COMPLETIONOVERRUN, LINEERR_INVALMESSAGEID.




## -remarks



This function is considered complete when the request is accepted by the network or switch; not when the request is fully completed in the way specified. When the called station or network enters a state where the call can be completed as requested, the service provider must send a 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> message with the call state equal to <i>offering</i>. The call's 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> record lists the reason for the call as CALLCOMPLETION and provides the completion identifier as well. It is possible to have multiple call completion requests outstanding at any given time; the maximum number is device dependent. The completion identifier is also used to refer to each individual request so requests can be canceled by calling 
<a href="https://msdn.microsoft.com/e8b5ee74-245f-4d91-8996-eec482241e4d">TSPI_lineUncompleteCall</a>.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/68f755a1-586b-4c5b-b8e8-c8b40eb71685">LINECALLCOMPLMODE_ Constants</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>



<a href="https://msdn.microsoft.com/e8b5ee74-245f-4d91-8996-eec482241e4d">TSPI_lineUncompleteCall</a>
 

 

