---
UID: NF:tapi.lineSetAgentMeasurementPeriod
title: lineSetAgentMeasurementPeriod function (tapi.h)
author: windows-sdk-content
description: The lineSetAgentMeasurementPeriod function sets the measurement period associated with a particular agent.
old-location: tapi2\linesetagentmeasurementperiod.htm
tech.root: Tapi
ms.assetid: bb84f18f-0052-45f8-8049-8576e1eb6fef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linesetagentmeasurementperiod, lineSetAgentMeasurementPeriod, lineSetAgentMeasurementPeriod function [TAPI 2.2], tapi/lineSetAgentMeasurementPeriod, tapi2.linesetagentmeasurementperiod"
ms.topic: function
f1_keywords: ["tapi/lineSetAgentMeasurementPeriod"]
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
 - lineSetAgentMeasurementPeriod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineSetAgentMeasurementPeriod function


## -description


The 
<b>lineSetAgentMeasurementPeriod</b> function sets the measurement period associated with a particular agent. It generates a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest_tag">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD.


## -parameters




### -param hLine

Handle to the line device.


### -param hAgent

Identifier of the agent whose information is to be changed.


### -param dwMeasurementPeriod

New measurement period (seconds). Must be greater than zero.


## -returns



Returns a request identifier if the asynchronous operation starts; otherwise, the function returns one of the following error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineproxyrequest_tag">LINEPROXYREQUEST</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a>
 

 

