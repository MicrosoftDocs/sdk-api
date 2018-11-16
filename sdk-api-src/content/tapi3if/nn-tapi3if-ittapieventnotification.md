---
UID: NN:tapi3if.ITTAPIEventNotification
title: ITTAPIEventNotification
author: windows-sdk-content
description: The ITTAPIEventNotification interface is an outgoing interface that allows an application to control the processing of event information.
old-location: tapi3\ittapieventnotification.htm
tech.root: Tapi
ms.assetid: 06cfe56c-907f-49ed-8a7a-db31383a06f9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITTAPIEventNotification, ITTAPIEventNotification interface [TAPI 2.2], ITTAPIEventNotification interface [TAPI 2.2],described, _tapi3_ittapieventnotification, tapi3.ittapieventnotification, tapi3if/ITTAPIEventNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPIEventNotification interface


## -description


The 
<b>ITTAPIEventNotification</b> interface is an outgoing interface that allows an application to control the processing of event information. The application must implement this interface: it must create a COM object that supports this interface, and then register it using the COM standard 
<a href="_com_iconnectionpointcontainer">IConnectionPointContainer</a> and 
<a href="_com_iconnectionpoint">IConnectionPoint</a> interfaces.

The 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method of this interface is called by TAPI in response to an event. Typically, the application implements a set of switch statements that use the value of a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> enumerator to determine the response to the event.

After registration of this interface, the application calls 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> to specify which events it must receive. If this method is not called, the application will not receive any events.

The application may then call 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> to notify TAPI of addresses and media types for which the application will accept incoming call sessions.

Please refer to the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Event</a> overview for additional information on event handling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPIEventNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITTAPIEventNotification</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">Event</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> descriptor for an asynchronous event notification.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Event overview</a>



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



<a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>



<a href="https://msdn.microsoft.com/788eee9c-b885-4b94-b259-694353c0f63a">ITDigitGenerationEvent</a>



<a href="https://msdn.microsoft.com/1199ec91-ee06-4e6c-8d8f-1585a3da3db0">ITParticipantEvent</a>



<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>



<a href="https://msdn.microsoft.com/7e4655ff-6ed4-4166-91f7-49d2e0556662">ITQueueEvent</a>



<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>



<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

