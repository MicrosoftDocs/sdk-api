---
UID: NF:tspi.TSPI_lineSetCallTreatment
title: TSPI_lineSetCallTreatment function
author: windows-sdk-content
description: The TSPI_lineSetCallTreatment function service provider stores the indicated dwCallTreatment in LINECALLINFO, and sends a LINE_CALLINFO message to indicate the updated information.
old-location: tspi\tspi_linesetcalltreatment.htm
old-project: tapi
ms.assetid: 04c93e35-df6b-409e-9bc4-06c36819963a
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineSetCallTreatment, TSPI_lineSetCallTreatment function [TAPI 2.2], _tspi_tspi_linesetcalltreatment, tspi.tspi_linesetcalltreatment, tspi/TSPI_lineSetCallTreatment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tspi.h
req.include-header: 
req.redist: 
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
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetCallTreatment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineSetCallTreatment function


## -description


The 
<b>TSPI_lineSetCallTreatment</b> function service provider stores the indicated <i>dwCallTreatment</i> in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>, and sends a 
<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a> message to indicate the updated information. If the call is currently in a state where the call treatment is relevant, the new treatment goes into effect at once; otherwise, it goes into effect the next time the call enters a relevant state.


## -parameters




### -param dwRequestID

Identifier for reporting asynchronous function results.


### -param hdCall

The service provider's handle to the call.


### -param dwTreatment

One of the call treatment identifiers supported on the address on which the call appears.


## -returns



Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, one of these negative error values:

LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a>
 

 

