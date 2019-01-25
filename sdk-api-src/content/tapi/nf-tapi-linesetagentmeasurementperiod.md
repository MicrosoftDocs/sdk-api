---
UID: NF:tapi.lineSetAgentMeasurementPeriod
title: lineSetAgentMeasurementPeriod function
author: windows-sdk-content
description: The lineSetAgentMeasurementPeriod function sets the measurement period associated with a particular agent.
old-location: tapi2\linesetagentmeasurementperiod.htm
tech.root: Tapi
ms.assetid: bb84f18f-0052-45f8-8049-8576e1eb6fef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linesetagentmeasurementperiod, lineSetAgentMeasurementPeriod, lineSetAgentMeasurementPeriod function [TAPI 2.2], tapi/lineSetAgentMeasurementPeriod, tapi2.linesetagentmeasurementperiod"
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
 - lineSetAgentMeasurementPeriod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetAgentMeasurementPeriod function


## -description


The 
<b>lineSetAgentMeasurementPeriod</b> function sets the measurement period associated with a particular agent. It generates a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message to be sent to a registered proxy function handler, referencing a 
<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a> structure of type LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD.


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




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>
 

 

