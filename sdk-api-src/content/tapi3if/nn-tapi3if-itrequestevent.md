---
UID: NN:tapi3if.ITRequestEvent
title: ITRequestEvent
author: windows-sdk-content
description: The ITRequestEvent interface contains methods that allow an application to receive and process Assisted Telephony request events.
old-location: tapi3\itrequestevent.htm
tech.root: tapi
ms.assetid: 69f9b504-be01-4167-8002-32a8e86bab0f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITRequestEvent, ITRequestEvent interface [TAPI 2.2], ITRequestEvent interface [TAPI 2.2],described, _tapi3_itrequestevent, tapi3.itrequestevent, tapi3if/ITRequestEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITRequestEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRequestEvent interface


## -description


The 
<b>ITRequestEvent</b> interface contains methods that allow an application to receive and process 
<a href="https://msdn.microsoft.com/1c41f52b-f8bf-410e-a966-9323a690a4d5">Assisted Telephony</a> request events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_REQUEST</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITRequestEvent</b> interface. The methods of this interface can be used to retrieve information concerning a request event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_REQUEST</b> event to enable reception of request events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITRequestEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITRequestEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITRequestEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d53fae21-4a4d-46ab-a0ff-48a7474b8782">get_AppName</a>
</td>
<td align="left" width="63%">
Gets the name of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dfbf033-83cf-4e2c-b107-963c10595ee5">get_CalledParty</a>
</td>
<td align="left" width="63%">
Gets the called party.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2150d521-cbd2-457f-b3c6-97761941a442">get_Comment</a>
</td>
<td align="left" width="63%">
Gets a comment associated with the request event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3cf5a48-6d9f-4c66-91eb-c18a29d71ff9">get_DestAddress</a>
</td>
<td align="left" width="63%">
Gets the destination address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fa157f8-fb4d-4163-b496-15bc28cca46b">get_RegistrationInstance</a>
</td>
<td align="left" width="63%">
Gets the registration instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c53d0ad-cb20-42f0-bd43-9b6bf18debcc">get_RequestMode</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/23321700-64d3-45e3-929a-8f5df64dc4be">request mode</a> descriptor.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2b6d4f99-3ffe-44ce-9cb5-3fdd565085db">ITRequest</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

