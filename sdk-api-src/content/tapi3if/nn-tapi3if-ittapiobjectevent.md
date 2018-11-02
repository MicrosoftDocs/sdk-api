---
UID: NN:tapi3if.ITTAPIObjectEvent
title: ITTAPIObjectEvent
author: windows-sdk-content
description: The ITTAPIObjectEvent interface contains methods that retrieve the description of TAPI object events.
old-location: tapi3\ittapiobjectevent.htm
tech.root: tapi
ms.assetid: 73be7109-0d3a-4ac5-adb7-e1577d8640b5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITTAPIObjectEvent, ITTAPIObjectEvent interface [TAPI 2.2], ITTAPIObjectEvent interface [TAPI 2.2],described, _tapi3_ittapiobjectevent, tapi3.ittapiobjectevent, tapi3if/ITTAPIObjectEvent
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
 - ITTAPIObjectEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPIObjectEvent interface


## -description


The 
<b>ITTAPIObjectEvent</b> interface contains methods that retrieve the description of TAPI object events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_TAPIOBJECT</b>, the method's <i>pEvent</i> parameter is an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> pointer for the 
<b>ITTAPIObjectEvent</b> interface. The methods of this interface can be used to retrieve information concerning the TAPI object change that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_TAPIOBJECT</b> event to enable reception of TAPI object events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>The 
<a href="https://msdn.microsoft.com/ad4fc838-5a6c-4942-b5a0-ed00cea11ba8">ITTAPIObjectEvent2</a> interface is an extension of the 
<b>ITTAPIObjectEvent</b> interface. 
<b>ITTAPIObjectEvent2</b> exposes an additional method that returns a pointer to an 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that caused the TAPI object event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPIObjectEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTAPIObjectEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPIObjectEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfe4ec23-42ae-4bb7-86cc-4d45d36b8817">get_Address</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13f16ccf-8d51-4f3f-90cb-3596cb8e9938">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Get the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ae4362f-6987-461e-928f-9478e37e0380">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> descriptor of an asynchronous event notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0dcf3ca-e6b7-4eb4-b3f2-8ddeea16d746">get_TAPIObject</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a> object on which the event occurred.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/ad4fc838-5a6c-4942-b5a0-ed00cea11ba8">ITTAPIObjectEvent2</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

