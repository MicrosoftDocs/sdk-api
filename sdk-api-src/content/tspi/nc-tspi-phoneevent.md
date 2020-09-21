---
UID: NC:tspi.PHONEEVENT
title: PHONEEVENT (tspi.h)
description: Phone_Event a callback function implemented by TAPI and supplied to the service provider as a parameter to TSPI_phoneOpen. The service provider calls this function to report events that occur on the phone.
helpviewer_keywords: ["PHONEEVENT","PHONEEVENT callback","Phone_Event","Phone_Event callback function [TAPI 2.2]","_tspi_phoneevent","tspi.phone_event_tspi","tspi.phoneevent","tspi/Phone_Event"]
old-location: tspi\phone_event_tspi.htm
tech.root: tapi3
ms.assetid: 0b5745a4-7652-48ce-9e8a-eef52c09455f
ms.date: 12/05/2018
ms.keywords: PHONEEVENT, PHONEEVENT callback, Phone_Event, Phone_Event callback function [TAPI 2.2], _tspi_phoneevent, tspi.phone_event_tspi, tspi.phoneevent, tspi/Phone_Event
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
 - PHONEEVENT
 - tspi/PHONEEVENT
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
 - Phone_Event
---

# PHONEEVENT callback function


## -description

<i>Phone_Event</i> a callback function implemented by TAPI and supplied to the service provider as a parameter to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phoneopen">TSPI_phoneOpen</a>. The service provider calls this function to report events that occur on the phone.

The <b>PHONEEVENT</b> type defines a pointer to this callback function. <i>Phone_Event</i> is a placeholder for the application-defined function name.

## -parameters

### -param htPhone

The TAPI handle for the phone on which the event occurred.

### -param dwMsg

Specifies the kind of event that is being reported. Interpretation of the other parameters is done in different ways according to the context indicated by <i>dwMsg</i>.

### -param dwParam1

A parameter for the message.

### -param dwParam2

A parameter for the message.

### -param dwParam3

A parameter for the message.

## -remarks

The call state when calling this function can be any state.

The service provider passes the 
<a href="/windows/desktop/Tapi/htapiphone">HTAPIPHONE</a> value supplied to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phoneopen">TSPI_phoneOpen</a> as the <i>htPhone</i> parameter. It includes the message identifier and parameters specific to the event.

The sets of messages that can be passed to this procedure differ slightly from the messages to the corresponding callback at the TAPI level. In particular, completion of asynchronously executing requests is reported through the 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">Completion_Proc</a> callback instead of this one.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">Completion_Proc</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>