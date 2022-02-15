---
UID: NF:tapi3if.ITAddress2.put_EventFilter
title: ITAddress2::put_EventFilter (tapi3if.h)
description: The put_EventFilter method sets an event filter for the current address. If no event filters are set, the application will not be notified of events on this address.
helpviewer_keywords: ["ITAddress2 interface [TAPI 2.2]","put_EventFilter method","ITAddress2.put_EventFilter","ITAddress2::put_EventFilter","_tapi3_itaddress2_put_eventfilter","put_EventFilter","put_EventFilter method [TAPI 2.2]","put_EventFilter method [TAPI 2.2]","ITAddress2 interface","tapi3.itaddress2_put_eventfilter","tapi3if/ITAddress2::put_EventFilter"]
old-location: tapi3\itaddress2_put_eventfilter.htm
tech.root: tapi3
ms.assetid: ca58c796-d843-48c3-9eac-ca126395d448
ms.date: 12/05/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],put_EventFilter method, ITAddress2.put_EventFilter, ITAddress2::put_EventFilter, _tapi3_itaddress2_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_put_eventfilter, tapi3if/ITAddress2::put_EventFilter
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAddress2::put_EventFilter
 - tapi3if/ITAddress2::put_EventFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress2.put_EventFilter
---

# ITAddress2::put_EventFilter


## -description

The 
<b>put_EventFilter</b> method sets an event filter for the current address. If no event filters are set, the application will not be notified of events on this address.

## -parameters

### -param TapiEvent [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> descriptor of the event type.

### -param lSubEvent [in]

Subevent descriptor.

### -param bEnable [in]

VARIANT_TRUE if the application requires notification of this event type. VARIANT_FALSE if the application does not require notifications for this event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>