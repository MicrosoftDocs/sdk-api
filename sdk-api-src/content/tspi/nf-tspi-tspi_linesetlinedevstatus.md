---
UID: NF:tspi.TSPI_lineSetLineDevStatus
title: TSPI_lineSetLineDevStatus function
author: windows-sdk-content
description: The TSPI_lineSetLineDevStatus service provider sets the device status as indicated, sending appropriate LINE_LINEDEVSTATE messages to indicate the new status.
old-location: tspi\tspi_linesetlinedevstatus.htm
tech.root: tapi
ms.assetid: 82afe6fd-a9fd-4e53-a460-370cab404366
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineSetLineDevStatus, TSPI_lineSetLineDevStatus function [TAPI 2.2], _tspi_tspi_linesetlinedevstatus, tspi.tspi_linesetlinedevstatus, tspi/TSPI_lineSetLineDevStatus
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
 - TSPI_lineSetLineDevStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineSetLineDevStatus function


## -description


The 
<b>TSPI_lineSetLineDevStatus</b> service provider sets the device status as indicated, sending appropriate 
<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a> messages to indicate the new status.


## -parameters




### -param dwRequestID

Identifier for reporting asynchronous function results.


### -param hdLine

The service provider's handle to the line device.


### -param dwStatusToChange

One or more of the 
<a href="https://msdn.microsoft.com/5fa754d3-07b2-4b75-91ef-1bf961d9fef4">LINEDEVSTATUSFLAGS_ constants</a>.


### -param fStatus

<b>TRUE</b> to turn on the indicated status bit(s), <b>FALSE</b> to turn off.


## -returns



Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALLINESTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a>
 

 

