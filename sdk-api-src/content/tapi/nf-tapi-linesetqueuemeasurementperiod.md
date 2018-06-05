---
UID: NF:tapi.lineSetQueueMeasurementPeriod
title: lineSetQueueMeasurementPeriod function
author: windows-sdk-content
description: The lineSetQueueMeasurementPeriod function sets the measurement period associated with a particular queue.
old-location: tapi2\linesetqueuemeasurementperiod.htm
old-project: Tapi
ms.assetid: 62b972ed-4a2d-4756-b905-dfb8c2bb0a8c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linesetqueuemeasurementperiod, lineSetQueueMeasurementPeriod, lineSetQueueMeasurementPeriod function [TAPI 2.2], tapi/lineSetQueueMeasurementPeriod, tapi2.linesetqueuemeasurementperiod"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineSetQueueMeasurementPeriod
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineSetQueueMeasurementPeriod function


## -description


The 
<b>lineSetQueueMeasurementPeriod</b> function sets the measurement period associated with a particular queue. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD.


## -parameters




### -param hLine

Handle to the line device.


### -param dwQueueID

Identifier of the queue whose information is to be changed.


### -param dwMeasurementPeriod

New measurement period (seconds). Must be greater than zero.


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

