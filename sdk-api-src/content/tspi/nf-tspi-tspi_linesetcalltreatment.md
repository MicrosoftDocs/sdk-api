---
UID: NF:tspi.TSPI_lineSetCallTreatment
title: TSPI_lineSetCallTreatment function (tspi.h)
description: The TSPI_lineSetCallTreatment function service provider stores the indicated dwCallTreatment in LINECALLINFO, and sends a LINE_CALLINFO message to indicate the updated information.
helpviewer_keywords: ["TSPI_lineSetCallTreatment","TSPI_lineSetCallTreatment function [TAPI 2.2]","_tspi_tspi_linesetcalltreatment","tspi.tspi_linesetcalltreatment","tspi/TSPI_lineSetCallTreatment"]
old-location: tspi\tspi_linesetcalltreatment.htm
tech.root: tapi3
ms.assetid: 04c93e35-df6b-409e-9bc4-06c36819963a
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallTreatment, TSPI_lineSetCallTreatment function [TAPI 2.2], _tspi_tspi_linesetcalltreatment, tspi.tspi_linesetcalltreatment, tspi/TSPI_lineSetCallTreatment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineSetCallTreatment
 - tspi/TSPI_lineSetCallTreatment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetCallTreatment
---

# TSPI_lineSetCallTreatment function


## -description

The 
<b>TSPI_lineSetCallTreatment</b> function service provider stores the indicated <i>dwCallTreatment</i> in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, and sends a 
<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a> message to indicate the updated information. If the call is currently in a state where the call treatment is relevant, the new treatment goes into effect at once; otherwise, it goes into effect the next time the call enters a relevant state.

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

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a>