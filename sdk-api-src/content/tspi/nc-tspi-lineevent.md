---
UID: NC:tspi.LINEEVENT
title: LINEEVENT (tspi.h)
description: Line_Event is a callback function implemented by TAPI and supplied to the service provider as a parameter to TSPI_lineOpen. The service provider calls this function to report events that occur on the line or on calls on the line.
helpviewer_keywords: ["LINEEVENT","LINEEVENT callback","Line_Event","Line_Event callback function [TAPI 2.2]","_tspi_lineevent","tspi.line_event","tspi.lineevent","tspi/Line_Event"]
old-location: tspi\line_event.htm
tech.root: tapi3
ms.assetid: 11ae7e78-8a10-4757-886b-c0aa47c4d55b
ms.date: 12/05/2018
ms.keywords: LINEEVENT, LINEEVENT callback, Line_Event, Line_Event callback function [TAPI 2.2], _tspi_lineevent, tspi.line_event, tspi.lineevent, tspi/Line_Event
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
 - LINEEVENT
 - tspi/LINEEVENT
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
 - Line_Event
---

# LINEEVENT callback function


## -description

<i>Line_Event</i> is a callback function implemented by TAPI and supplied to the service provider as a parameter to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>. The service provider calls this function to report events that occur on the line or on calls on the line.

The <b>LINEEVENT</b> type defines a pointer to this callback function. <i>Line_Event</i> is a placeholder for the application-defined function name.

## -parameters

### -param htLine

The TAPI handle for the line on which the event occurred.

### -param htCall

The TAPI handle for the call on which the event occurred if this is a call-related event. For line-related events where there is no call, this parameter is set to <b>NULL</b>.

### -param dwMsg

Specifies the kind of event that is being reported. Interpretation of the other parameters is performed in different ways according to the context indicated by <i>dwMsg</i>.

### -param dwParam1

A parameter for the message.

### -param dwParam2

A parameter for the message.

### -param dwParam3

A parameter for the message.

## -remarks

The call state when calling this function can be any state.

The service provider passes the 
<a href="/windows/desktop/Tapi/htapiline">HTAPILINE</a> value supplied to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a> as the <i>htLine</i> parameter. It includes the message identifier and parameters specific to the event.

This function differs from the callback function defined at the TAPI level in that it separates line and call parameters. Both parameters are used for some messages. The sets of messages that can be passed to this procedure differ slightly from the TAPI level. In particular, completion of asynchronously executing requests is reported through the 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">Completion_Proc</a> callback instead of this one.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">Completion_Proc</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>