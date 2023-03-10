---
UID: NE:tapi3if.TAPI_EVENT
title: TAPI_EVENT (tapi3if.h)
description: Used to notify an application that a change has occurred in the TAPI object.
helpviewer_keywords: ["TAPI_EVENT","TAPI_EVENT enumeration [TAPI 2.2]","TE_ACDGROUP","TE_ADDRESS","TE_ADDRESSDEVSPECIFIC","TE_AGENT","TE_AGENTHANDLER","TE_AGENTSESSION","TE_ASRTERMINAL","TE_CALLHUB","TE_CALLINFOCHANGE","TE_CALLMEDIA","TE_CALLNOTIFICATION","TE_CALLSTATE","TE_DIGITEVENT","TE_FILETERMINAL","TE_GATHERDIGITS","TE_GENERATEEVENT","TE_PHONEDEVSPECIFIC","TE_PHONEEVENT","TE_PRIVATE","TE_QOSEVENT","TE_QUEUE","TE_REQUEST","TE_TAPIOBJECT","TE_TONEEVENT","TE_TONETERMINAL","TE_TTSTERMINAL","_tapi3_tapi_event","tapi3.tapi_event","tapi3if/TAPI_EVENT","tapi3if/TE_ACDGROUP","tapi3if/TE_ADDRESS","tapi3if/TE_ADDRESSDEVSPECIFIC","tapi3if/TE_AGENT","tapi3if/TE_AGENTHANDLER","tapi3if/TE_AGENTSESSION","tapi3if/TE_ASRTERMINAL","tapi3if/TE_CALLHUB","tapi3if/TE_CALLINFOCHANGE","tapi3if/TE_CALLMEDIA","tapi3if/TE_CALLNOTIFICATION","tapi3if/TE_CALLSTATE","tapi3if/TE_DIGITEVENT","tapi3if/TE_FILETERMINAL","tapi3if/TE_GATHERDIGITS","tapi3if/TE_GENERATEEVENT","tapi3if/TE_PHONEDEVSPECIFIC","tapi3if/TE_PHONEEVENT","tapi3if/TE_PRIVATE","tapi3if/TE_QOSEVENT","tapi3if/TE_QUEUE","tapi3if/TE_REQUEST","tapi3if/TE_TAPIOBJECT","tapi3if/TE_TONEEVENT","tapi3if/TE_TONETERMINAL","tapi3if/TE_TTSTERMINAL"]
old-location: tapi3\tapi_event.htm
tech.root: tapi3
ms.assetid: 94faa4a1-7d86-48bc-9e94-f2b8f83f5280
ms.date: 12/05/2018
ms.keywords: TAPI_EVENT, TAPI_EVENT enumeration [TAPI 2.2], TE_ACDGROUP, TE_ADDRESS, TE_ADDRESSDEVSPECIFIC, TE_AGENT, TE_AGENTHANDLER, TE_AGENTSESSION, TE_ASRTERMINAL, TE_CALLHUB, TE_CALLINFOCHANGE, TE_CALLMEDIA, TE_CALLNOTIFICATION, TE_CALLSTATE, TE_DIGITEVENT, TE_FILETERMINAL, TE_GATHERDIGITS, TE_GENERATEEVENT, TE_PHONEDEVSPECIFIC, TE_PHONEEVENT, TE_PRIVATE, TE_QOSEVENT, TE_QUEUE, TE_REQUEST, TE_TAPIOBJECT, TE_TONEEVENT, TE_TONETERMINAL, TE_TTSTERMINAL, _tapi3_tapi_event, tapi3.tapi_event, tapi3if/TAPI_EVENT, tapi3if/TE_ACDGROUP, tapi3if/TE_ADDRESS, tapi3if/TE_ADDRESSDEVSPECIFIC, tapi3if/TE_AGENT, tapi3if/TE_AGENTHANDLER, tapi3if/TE_AGENTSESSION, tapi3if/TE_ASRTERMINAL, tapi3if/TE_CALLHUB, tapi3if/TE_CALLINFOCHANGE, tapi3if/TE_CALLMEDIA, tapi3if/TE_CALLNOTIFICATION, tapi3if/TE_CALLSTATE, tapi3if/TE_DIGITEVENT, tapi3if/TE_FILETERMINAL, tapi3if/TE_GATHERDIGITS, tapi3if/TE_GENERATEEVENT, tapi3if/TE_PHONEDEVSPECIFIC, tapi3if/TE_PHONEEVENT, tapi3if/TE_PRIVATE, tapi3if/TE_QOSEVENT, tapi3if/TE_QUEUE, tapi3if/TE_REQUEST, tapi3if/TE_TAPIOBJECT, tapi3if/TE_TONEEVENT, tapi3if/TE_TONETERMINAL, tapi3if/TE_TTSTERMINAL
req.header: tapi3if.h
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
req.typenames: TAPI_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TAPI_EVENT
 - tapi3if/TAPI_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPI_EVENT
---

# TAPI_EVENT enumeration


## -description

The 
<b>TAPI_EVENT</b> enumeration is used to notify an application that a change has occurred in the TAPI object. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method implementation uses members of this enumeration to indicate the type of object associated with the <b>IDispatch</b> pointer passed by TAPI.

## -enum-fields

### -field TE_TAPIOBJECT:0x1

Change is in TAPI object itself. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>.

### -field TE_ADDRESS:0x2

An Address object has changed. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent">ITAddressEvent</a>.

### -field TE_CALLNOTIFICATION:0x4

A new communications session has appeared on the address and the TAPI DLL has created a new call object. This could be a result from an incoming session, a session handed off by another application, or a session being parked on the address. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>.

### -field TE_CALLSTATE:0x8

The Call state has changed. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>.

### -field TE_CALLMEDIA:0x10

The media associated with a call has changed. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>.

### -field TE_CALLHUB:0x20

A CallHub object has changed. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>.

### -field TE_CALLINFOCHANGE:0x40

The call information has changed. 
For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent">ITCallInfoChangeEvent</a>.

### -field TE_PRIVATE:0x80

A provider-specific private object has changed. The precise type of object referenced is implementation dependent. For more information, see <a href="/windows/desktop/Tapi/provider-specific-interfaces">Provider-Specific Interfaces</a>.

### -field TE_REQUEST:0x100

A Request object has changed. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>.

### -field TE_AGENT:0x200

An Agent object has changed. For more information, see <a href="/windows/desktop/api/tapi3/nn-tapi3-itagentevent">ITAgentEvent</a>.

### -field TE_AGENTSESSION:0x400

An AgentSession object has changed. For more information, see <a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsessionevent">ITAgentSessionEvent</a>.

### -field TE_QOSEVENT:0x800

A QOS event has occurred. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>.

### -field TE_AGENTHANDLER:0x1000

An AgentHandler object has changed. For more information, see <a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandlerevent">ITAgentHandlerEvent</a>.

### -field TE_ACDGROUP:0x2000

An ACDGroup object has changed. For more information, see <a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroupevent">ITACDGroupEvent</a>.

### -field TE_QUEUE:0x4000

A Queue object has changed. For more information, see <a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueueevent">ITQueueEvent</a>.

### -field TE_DIGITEVENT:0x8000

A digit event has occurred. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitdetectionevent">ITDigitDetectionEvent</a>.

### -field TE_GENERATEEVENT:0x10000

A digit generation event has occurred. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitgenerationevent">ITDigitGenerationEvent</a>.

### -field TE_ASRTERMINAL:0x20000

An Automatic Speech Recognition terminal event has occurred. Valid only for computers running on Windows XP and later.

### -field TE_TTSTERMINAL:0x40000

An event has occurred on a TTS terminal. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent">ITTTSTerminalEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_FILETERMINAL:0x80000

An event has occurred on a file terminal. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_TONETERMINAL:0x100000

An event has occurred on a tone terminal. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent">ITToneTerminalEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_PHONEEVENT:0x200000

A Phone object has changed. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_TONEEVENT:0x400000

A tone event has been fired. Detection of in-band tones will be enabled or disabled. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittonedetectionevent">ITToneDetectionEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_GATHERDIGITS:0x800000

A gather digits event has been fired. Digits will be gathered on the current call. For more information, see 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitsgatheredevent">ITDigitsGatheredEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_ADDRESSDEVSPECIFIC:0x1000000

An address device-specific event has occurred. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressdevicespecificevent">ITAddressDeviceSpecificEvent</a>. Valid only for computers running on Windows XP and later.

### -field TE_PHONEDEVSPECIFIC:0x2000000

A phone device-specific event has occurred. For more information, see <a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressdevicespecificevent">ITPhoneDeviceSpecificEvent</a>. Valid only for computers running on Windows XP and later.

## -remarks

Call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set the event filter mask to enable receiving events. If <b>ITTAPI::put_EventFilter</b> is not called, the application cannot receive events.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroupevent">ITACDGroupEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent">ITAddressEvent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentevent">ITAgentEvent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandlerevent">ITAgentHandlerEvent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsessionevent">ITAgentSessionEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent">ITCallInfoChangeEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueueevent">ITQueueEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>
