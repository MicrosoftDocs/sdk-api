---
UID: NN:tapi3if.ITCallStateEvent
title: ITCallStateEvent
author: windows-sdk-content
description: The ITCallStateEvent interface contains methods that retrieve the description of call state events.
old-location: tapi3\itcallstateevent.htm
old-project: Tapi
ms.assetid: 0885ef81-726d-41ca-be8c-b3ff2e02fc3c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITCallStateEvent, ITCallStateEvent interface [TAPI 2.2], ITCallStateEvent interface [TAPI 2.2],described, _tapi3_itcallstateevent, tapi3.itcallstateevent, tapi3if/ITCallStateEvent
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallStateEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallStateEvent interface


## -description


The 
<b>ITCallStateEvent</b> interface contains methods that retrieve the description of call state events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_CALLSTATE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallStateEvent</b> interface. The methods of this interface can be used to retrieve information concerning the change that has occurred in the call state.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLSTATE</b> event to enable reception of call state events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallStateEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITCallStateEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallStateEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/942bd437-77d1-4d06-91d3-138b06f3228e">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4add561-94be-44e2-84bb-89d1e5e98969">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3a4b985-1c0f-4e93-a965-c61c9c0ab10d">get_Cause</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/9bc9e050-41f7-4330-a263-db745d3fa3f8">CALL_STATE_EVENT_CAUSE</a> descriptor of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45e46b99-c65f-4296-9537-7fb7a4210727">get_State</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">CALL_STATE</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">CALL_STATE</a>



<a href="https://msdn.microsoft.com/9bc9e050-41f7-4330-a263-db745d3fa3f8">CALL_STATE_EVENT_CAUSE</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

