---
UID: NN:tapi3if.ITASRTerminalEvent
title: ITASRTerminalEvent (tapi3if.h)
description: The ITASRTerminalEvent interface contains methods that retrieve the description of Automatic Speech Recognition terminal events that have occurred.
helpviewer_keywords: ["ITASRTerminalEvent","ITASRTerminalEvent interface [TAPI 2.2]","ITASRTerminalEvent interface [TAPI 2.2]","described","_tapi3_itasrterminalevent","tapi3.itasrterminalevent","tapi3if/ITASRTerminalEvent"]
old-location: tapi3\itasrterminalevent.htm
tech.root: tapi3
ms.assetid: 6bf8b1b7-698f-443f-9ddf-0d50551cebab
ms.date: 12/05/2018
ms.keywords: ITASRTerminalEvent, ITASRTerminalEvent interface [TAPI 2.2], ITASRTerminalEvent interface [TAPI 2.2],described, _tapi3_itasrterminalevent, tapi3.itasrterminalevent, tapi3if/ITASRTerminalEvent
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
 - ITASRTerminalEvent
 - tapi3if/ITASRTerminalEvent
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
 - ITASRTerminalEvent
---

# ITASRTerminalEvent interface


## -description

The 
<b>ITASRTerminalEvent</b> interface contains methods that retrieve the description of Automatic Speech Recognition terminal events that have occurred. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_ASRTERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITASRTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_ASRTERMINAL</b> to enable reception of Automatic Speech Recognition terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITASRTerminalEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITASRTerminalEvent</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
