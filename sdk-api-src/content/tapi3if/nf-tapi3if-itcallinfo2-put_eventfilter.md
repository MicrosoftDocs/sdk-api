---
UID: NF:tapi3if.ITCallInfo2.put_EventFilter
title: ITCallInfo2::put_EventFilter (tapi3if.h)
description: The put_EventFilter method sets an event filter for the current call.
helpviewer_keywords: ["ITCallInfo2 interface [TAPI 2.2]","put_EventFilter method","ITCallInfo2.put_EventFilter","ITCallInfo2::put_EventFilter","_tapi3_itcallinfo2_put_eventfilter","put_EventFilter","put_EventFilter method [TAPI 2.2]","put_EventFilter method [TAPI 2.2]","ITCallInfo2 interface","tapi3.itcallinfo2_put_eventfilter","tapi3if/ITCallInfo2::put_EventFilter"]
old-location: tapi3\itcallinfo2_put_eventfilter.htm
tech.root: tapi3
ms.assetid: 8e1b4474-b9ff-489d-8226-58eda659e057
ms.date: 12/05/2018
ms.keywords: ITCallInfo2 interface [TAPI 2.2],put_EventFilter method, ITCallInfo2.put_EventFilter, ITCallInfo2::put_EventFilter, _tapi3_itcallinfo2_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITCallInfo2 interface, tapi3.itcallinfo2_put_eventfilter, tapi3if/ITCallInfo2::put_EventFilter
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
 - ITCallInfo2::put_EventFilter
 - tapi3if/ITCallInfo2::put_EventFilter
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
 - ITCallInfo2.put_EventFilter
---

# ITCallInfo2::put_EventFilter


## -description

The 
<b>put_EventFilter</b> method sets an event filter for the current call.

## -parameters

### -param TapiEvent [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> descriptor of the event type.

### -param lSubEvent [in]

Subevent descriptor.

### -param bEnable [in]

VARIANT_TRUE if application requires notification of this event type. VARIANT_FALSE indicates the application does not require notifications for this event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2">ITCallInfo2</a>