---
UID: NF:tapi3.ITPluggableTerminalEventSink.FireEvent
title: ITPluggableTerminalEventSink::FireEvent (tapi3.h)
description: The ITPluggableTerminalEventSink::FireEvent (tapi3.h) method results in a message that notifies the client application of a change in the pluggable terminal.
helpviewer_keywords: ["FireEvent","FireEvent method [TAPI 2.2]","FireEvent method [TAPI 2.2]","ITPluggableTerminalEventSink interface","ITPluggableTerminalEventSink interface [TAPI 2.2]","FireEvent method","ITPluggableTerminalEventSink.FireEvent","ITPluggableTerminalEventSink::FireEvent","_tapi3_itpluggableterminaleventsink_fireevent","msp/ITPluggableTerminalEventSink::FireEvent","tapi3.itpluggableterminaleventsink_fireevent"]
old-location: tapi3\itpluggableterminaleventsink_fireevent.htm
tech.root: tapi3
ms.assetid: 67386c32-5714-4b01-b860-25192349aa6c
ms.date: 08/09/2022
ms.keywords: FireEvent, FireEvent method [TAPI 2.2], FireEvent method [TAPI 2.2],ITPluggableTerminalEventSink interface, ITPluggableTerminalEventSink interface [TAPI 2.2],FireEvent method, ITPluggableTerminalEventSink.FireEvent, ITPluggableTerminalEventSink::FireEvent, _tapi3_itpluggableterminaleventsink_fireevent, msp/ITPluggableTerminalEventSink::FireEvent, tapi3.itpluggableterminaleventsink_fireevent
req.header: tapi3.h
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
 - ITPluggableTerminalEventSink::FireEvent
 - tapi3/ITPluggableTerminalEventSink::FireEvent
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
 - ITPluggableTerminalEventSink.FireEvent
---

# ITPluggableTerminalEventSink::FireEvent


## -description

The 
<b>FireEvent</b> method results in a message that notifies the client application of a change in the pluggable terminal. For example, if the terminal is no longer available, the <b>event</b> member of the 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> structure is set to <b>ME_ADDRESS_EVENT</b> and the <b>type</b> member is set to <b>ADDRESS_TERMINAL_UNAVAILABLE</b>.

## -parameters

### -param pMspEventInfo [in]

Pointer to a const cast of the 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> structure.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink">ITPluggableTerminalEventSink</a>



<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>
