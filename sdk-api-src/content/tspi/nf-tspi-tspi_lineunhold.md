---
UID: NF:tspi.TSPI_lineUnhold
title: TSPI_lineUnhold function
author: windows-sdk-content
description: The TSPI_lineUnhold function retrieves the specified held call.
old-location: tspi\tspi_lineunhold.htm
tech.root: tapi
ms.assetid: 4719c399-0dce-4aa2-9b6e-a84ad13f9228
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: TSPI_lineUnhold, TSPI_lineUnhold function [TAPI 2.2], _tspi_tspi_lineunhold, tspi.tspi_lineunhold, tspi/TSPI_lineUnhold
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
 - TSPI_lineUnhold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineUnhold function


## -description


The 
<b>TSPI_lineUnhold</b> function retrieves the specified held call.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call to be retrieved. The call state of <i>hdCall</i> can be <i>onHold</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provider returns LINEERR_INVALCALLSTATE if the call is not currently on hold.

This operation works for calls on hard hold (calls placed on hold using 
<a href="https://msdn.microsoft.com/395aa8cc-fdbf-4772-940b-ea5944b26812">TSPI_lineHold</a>) and on soft hold. The service provider should check that the call is currently in the <i>onHold</i>, <i>onHoldPendingTransfer</i>, or <i>onHoldPendingConference</i> state, change the state to <i>connected</i>, and send a LINECALLSTATE message for the new call state.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/395aa8cc-fdbf-4772-940b-ea5944b26812">TSPI_lineHold</a>
 

 

