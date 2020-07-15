---
UID: NF:tapi.lineSetQueueMeasurementPeriod
title: lineSetQueueMeasurementPeriod function (tapi.h)
description: The lineSetQueueMeasurementPeriod function sets the measurement period associated with a particular queue.
helpviewer_keywords: ["_tapi2_linesetqueuemeasurementperiod","lineSetQueueMeasurementPeriod","lineSetQueueMeasurementPeriod function [TAPI 2.2]","tapi/lineSetQueueMeasurementPeriod","tapi2.linesetqueuemeasurementperiod"]
old-location: tapi2\linesetqueuemeasurementperiod.htm
tech.root: Tapi
ms.assetid: 62b972ed-4a2d-4756-b905-dfb8c2bb0a8c
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetqueuemeasurementperiod, lineSetQueueMeasurementPeriod, lineSetQueueMeasurementPeriod function [TAPI 2.2], tapi/lineSetQueueMeasurementPeriod, tapi2.linesetqueuemeasurementperiod
f1_keywords:
- tapi/lineSetQueueMeasurementPeriod
dev_langs:
- c++
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
- lineSetQueueMeasurementPeriod
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineSetQueueMeasurementPeriod function


## -description


The 
<b>lineSetQueueMeasurementPeriod</b> function sets the measurement period associated with a particular queue. It generates a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD.


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




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>
 

 

