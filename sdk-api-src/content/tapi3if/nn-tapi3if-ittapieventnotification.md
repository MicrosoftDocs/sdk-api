---
UID: NN:tapi3if.ITTAPIEventNotification
title: ITTAPIEventNotification (tapi3if.h)
author: windows-sdk-content
description: The ITTAPIEventNotification interface is an outgoing interface that allows an application to control the processing of event information.
old-location: tapi3\ittapieventnotification.htm
tech.root: Tapi
ms.assetid: 06cfe56c-907f-49ed-8a7a-db31383a06f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTAPIEventNotification, ITTAPIEventNotification interface [TAPI 2.2], ITTAPIEventNotification interface [TAPI 2.2],described, _tapi3_ittapieventnotification, tapi3.ittapieventnotification, tapi3if/ITTAPIEventNotification
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITTAPIEventNotification"
dev_langs:
 - c++
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPIEventNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPIEventNotification interface


## -description


The 
<b>ITTAPIEventNotification</b> interface is an outgoing interface that allows an application to control the processing of event information. The application must implement this interface: it must create a COM object that supports this interface, and then register it using the COM standard 
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interfaces.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method of this interface is called by TAPI in response to an event. Typically, the application implements a set of switch statements that use the value of a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> enumerator to determine the response to the event.

After registration of this interface, the application calls 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> to specify which events it must receive. If this method is not called, the application will not receive any events.

The application may then call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a> to notify TAPI of addresses and media types for which the application will accept incoming call sessions.

Please refer to the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Event</a> overview for additional information on event handling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPIEventNotification</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITTAPIEventNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPIEventNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">Event</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> descriptor for an asynchronous event notification.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Event overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itacdgroupevent">ITACDGroupEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent">ITAddressEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagentevent">ITAgentEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandlerevent">ITAgentHandlerEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagentsessionevent">ITAgentSessionEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent">ITCallInfoChangeEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent">ITCallMediaEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent">ITCallStateEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itdigitdetectionevent">ITDigitDetectionEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itdigitgenerationevent">ITDigitGenerationEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/itparticipantevent">ITParticipantEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueueevent">ITQueueEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
 

 

