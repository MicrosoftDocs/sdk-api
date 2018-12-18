---
UID: NE:tapi3if.TAPI_EVENT
title: TAPI_EVENT
author: windows-sdk-content
description: Used to notify an application that a change has occurred in the TAPI object.
old-location: tapi3\tapi_event.htm
tech.root: tapi
ms.assetid: 94faa4a1-7d86-48bc-9e94-f2b8f83f5280
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TAPI_EVENT, TAPI_EVENT enumeration [TAPI 2.2], TE_ACDGROUP, TE_ADDRESS, TE_ADDRESSDEVSPECIFIC, TE_AGENT, TE_AGENTHANDLER, TE_AGENTSESSION, TE_ASRTERMINAL, TE_CALLHUB, TE_CALLINFOCHANGE, TE_CALLMEDIA, TE_CALLNOTIFICATION, TE_CALLSTATE, TE_DIGITEVENT, TE_FILETERMINAL, TE_GATHERDIGITS, TE_GENERATEEVENT, TE_PHONEDEVSPECIFIC, TE_PHONEEVENT, TE_PRIVATE, TE_QOSEVENT, TE_QUEUE, TE_REQUEST, TE_TAPIOBJECT, TE_TONEEVENT, TE_TONETERMINAL, TE_TTSTERMINAL, _tapi3_tapi_event, tapi3.tapi_event, tapi3if/TAPI_EVENT, tapi3if/TE_ACDGROUP, tapi3if/TE_ADDRESS, tapi3if/TE_ADDRESSDEVSPECIFIC, tapi3if/TE_AGENT, tapi3if/TE_AGENTHANDLER, tapi3if/TE_AGENTSESSION, tapi3if/TE_ASRTERMINAL, tapi3if/TE_CALLHUB, tapi3if/TE_CALLINFOCHANGE, tapi3if/TE_CALLMEDIA, tapi3if/TE_CALLNOTIFICATION, tapi3if/TE_CALLSTATE, tapi3if/TE_DIGITEVENT, tapi3if/TE_FILETERMINAL, tapi3if/TE_GATHERDIGITS, tapi3if/TE_GENERATEEVENT, tapi3if/TE_PHONEDEVSPECIFIC, tapi3if/TE_PHONEEVENT, tapi3if/TE_PRIVATE, tapi3if/TE_QOSEVENT, tapi3if/TE_QUEUE, tapi3if/TE_REQUEST, tapi3if/TE_TAPIOBJECT, tapi3if/TE_TONEEVENT, tapi3if/TE_TONETERMINAL, tapi3if/TE_TTSTERMINAL
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPI_EVENT
product: Windows
targetos: Windows
req.typenames: TAPI_EVENT
req.redist: 
---

# TAPI_EVENT enumeration


## -description


The 
<b>TAPI_EVENT</b> enumeration is used to notify an application that a change has occurred in the TAPI object. The 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method implementation uses members of this enumeration to indicate the type of object associated with the <b>IDispatch</b> pointer passed by TAPI.


## -enum-fields




### -field TE_TAPIOBJECT

Change is in TAPI object itself. For more information, see 
<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a>.


### -field TE_ADDRESS

An Address object has changed. For more information, see 
<a href="https://msdn.microsoft.com/340d938a-a107-4317-af65-3dca98102767">ITAddressEvent</a>.


### -field TE_CALLNOTIFICATION

A new communications session has appeared on the address and the TAPI DLL has created a new call object. This could be a result from an incoming session, a session handed off by another application, or a session being parked on the address. For more information, see 
<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a> and 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>.


### -field TE_CALLSTATE

The Call state has changed. For more information, see 
<a href="https://msdn.microsoft.com/0885ef81-726d-41ca-be8c-b3ff2e02fc3c">ITCallStateEvent</a>.


### -field TE_CALLMEDIA

The media associated with a call has changed. For more information, see 
<a href="https://msdn.microsoft.com/db55ff03-9271-4a94-9cba-a3ef0282b7b6">ITCallMediaEvent</a>.


### -field TE_CALLHUB

A CallHub object has changed. For more information, see 
<a href="https://msdn.microsoft.com/4008fc7e-f095-442d-9214-61bfead8cf04">ITCallHubEvent</a>.


### -field TE_CALLINFOCHANGE

The call information has changed. 
For more information, see <a href="https://msdn.microsoft.com/f543da95-c0cc-4631-b91e-ba02dde2c081">ITCallInfoChangeEvent</a>.


### -field TE_PRIVATE

A provider-specific private object has changed. The precise type of object referenced is implementation dependent. For more information, see <a href="https://msdn.microsoft.com/8077c9a7-3235-41a7-97dc-ca5f3c291ee6">Provider-Specific Interfaces</a>.


### -field TE_REQUEST

A Request object has changed. For more information, see <a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>.


### -field TE_AGENT

An Agent object has changed. For more information, see <a href="https://msdn.microsoft.com/adfb58f7-b02c-4a64-92c1-a1b29c9f7143">ITAgentEvent</a>.


### -field TE_AGENTSESSION

An AgentSession object has changed. For more information, see <a href="https://msdn.microsoft.com/70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b">ITAgentSessionEvent</a>.


### -field TE_QOSEVENT

A QOS event has occurred. For more information, see <a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>.


### -field TE_AGENTHANDLER

An AgentHandler object has changed. For more information, see <a href="https://msdn.microsoft.com/c61becce-09fd-4b12-bbc9-98df57d5f0d3">ITAgentHandlerEvent</a>.


### -field TE_ACDGROUP

An ACDGroup object has changed. For more information, see <a href="https://msdn.microsoft.com/5770dca5-cf71-4211-ba9f-0fe7a3bbb614">ITACDGroupEvent</a>.


### -field TE_QUEUE

A Queue object has changed. For more information, see <a href="https://msdn.microsoft.com/7e4655ff-6ed4-4166-91f7-49d2e0556662">ITQueueEvent</a>.


### -field TE_DIGITEVENT

A digit event has occurred. For more information, see <a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>.


### -field TE_GENERATEEVENT

A digit generation event has occurred. For more information, see <a href="https://msdn.microsoft.com/788eee9c-b885-4b94-b259-694353c0f63a">ITDigitGenerationEvent</a>.


### -field TE_ASRTERMINAL

An Automatic Speech Recognition terminal event has occurred. Valid only for computers running on Windows XP and later.


### -field TE_TTSTERMINAL

An event has occurred on a TTS terminal. For more information, see <a href="https://msdn.microsoft.com/0375d6e4-cd9f-4245-abf5-1b200af79848">ITTTSTerminalEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_FILETERMINAL

An event has occurred on a file terminal. For more information, see <a href="https://msdn.microsoft.com/cb6f2869-ec31-49ac-873b-35a0dcd2c8d7">ITFileTerminalEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_TONETERMINAL

An event has occurred on a tone terminal. For more information, see <a href="https://msdn.microsoft.com/6a5d03e9-e6d1-452a-a189-ca693a72c610">ITToneTerminalEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_PHONEEVENT

A Phone object has changed. For more information, see 
<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_TONEEVENT

A tone event has been fired. Detection of in-band tones will be enabled or disabled. For more information, see 
<a href="https://msdn.microsoft.com/1e0f71a2-1aae-46b7-9147-7bf9da4d9503">ITToneDetectionEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_GATHERDIGITS

A gather digits event has been fired. Digits will be gathered on the current call. For more information, see 
<a href="https://msdn.microsoft.com/2d710bea-a0fd-492b-81a3-03b741685c91">ITDigitsGatheredEvent</a>. Valid only for computers running on Windows XP and later.


### -field TE_ADDRESSDEVSPECIFIC

An address device-specific event has occurred. For more information, see <a href="https://msdn.microsoft.com/8590e9b1-2bbf-47e5-96de-8765a475a972">ITAddressDeviceSpecificEvent</a>. Valid only for computers running on Windows XP and later.



### -field TE_PHONEDEVSPECIFIC

A phone device-specific event has occurred. For more information, see <a href="https://msdn.microsoft.com/8590e9b1-2bbf-47e5-96de-8765a475a972">ITPhoneDeviceSpecificEvent</a>. Valid only for computers running on Windows XP and later.


## -remarks



Call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set the event filter mask to enable receiving events. If <b>ITTAPI::put_EventFilter</b> is not called, the application cannot receive events.




## -see-also




<a href="https://msdn.microsoft.com/5770dca5-cf71-4211-ba9f-0fe7a3bbb614">ITACDGroupEvent</a>



<a href="https://msdn.microsoft.com/340d938a-a107-4317-af65-3dca98102767">ITAddressEvent</a>



<a href="https://msdn.microsoft.com/adfb58f7-b02c-4a64-92c1-a1b29c9f7143">ITAgentEvent</a>



<a href="https://msdn.microsoft.com/c61becce-09fd-4b12-bbc9-98df57d5f0d3">ITAgentHandlerEvent</a>



<a href="https://msdn.microsoft.com/70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b">ITAgentSessionEvent</a>



<a href="https://msdn.microsoft.com/4008fc7e-f095-442d-9214-61bfead8cf04">ITCallHubEvent</a>



<a href="https://msdn.microsoft.com/f543da95-c0cc-4631-b91e-ba02dde2c081">ITCallInfoChangeEvent</a>



<a href="https://msdn.microsoft.com/db55ff03-9271-4a94-9cba-a3ef0282b7b6">ITCallMediaEvent</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>



<a href="https://msdn.microsoft.com/0885ef81-726d-41ca-be8c-b3ff2e02fc3c">ITCallStateEvent</a>



<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>



<a href="https://msdn.microsoft.com/7e4655ff-6ed4-4166-91f7-49d2e0556662">ITQueueEvent</a>



<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a>
 

 

