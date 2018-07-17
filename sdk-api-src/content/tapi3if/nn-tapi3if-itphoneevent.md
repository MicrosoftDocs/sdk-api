---
UID: NN:tapi3if.ITPhoneEvent
title: ITPhoneEvent
author: windows-sdk-content
description: The ITPhoneEvent interface contains methods that retrieve the description of phone events that have occurred.
old-location: tapi3\itphoneevent.htm
old-project: tapi
ms.assetid: cc3ca533-d523-4889-b3c7-bb306e49b85b
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPhoneEvent, ITPhoneEvent interface [TAPI 2.2], ITPhoneEvent interface [TAPI 2.2],described, _tapi3_itphoneevent, tapi3.itphoneevent, tapi3if/ITPhoneEvent
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
 - ITPhoneEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneEvent interface


## -description


The 
<b>ITPhoneEvent</b> interface contains methods that retrieve the description of phone events that have occurred. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_PHONEEVENT</b>, the method's <i>pEvent</i> parameter is an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer for the 
<b>ITPhoneEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_PHONEEVENT</b> to enable reception of phone events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhoneEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITPhoneEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPhoneEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43b87d10-8cb9-4795-8778-70c8f8ae6300">get_ButtonLampId</a>
</td>
<td align="left" width="63%">
Gets a long value indicating which button or lamp triggered the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eedda9d-c127-446d-972c-09a7c1a4bd0f">get_ButtonState</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/a9f7b527-9c74-45ac-9394-6f736aae1ccf">PHONE_BUTTON_STATE</a> value specifying the state to which the button has transitioned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52305981-d97a-4b7c-9886-6e2543bd1a27">get_Call</a>
</td>
<td align="left" width="63%">
Gets pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">get_Event</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/9508cb8f-b7c9-4d5c-a58d-afdf079f9fee">PHONE_EVENT</a> value specifying the type of phone event that occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acc25e8e-966f-4b54-ad59-226d2b7728b8">get_HookSwitchDevice</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/20b17e2f-f745-41ef-91ac-d2ab21d43695">PHONE_HOOK_SWITCH_DEVICE</a> value specifying the hookswitch device that changed state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7d1033d-0a37-4b9c-86d7-bab5a2cbb454">get_HookSwitchState</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/c9501a3f-1aaa-4d58-aca1-5ef00c31d195">PHONE_HOOK_SWITCH_STATE</a> value specifying the state to which the hookswitch has transitioned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04537dbb-e1a1-445c-963e-13a8733f2566">get_NumberGathered</a>
</td>
<td align="left" width="63%">
Returns a <b>BSTR</b> value specifying the phone number that was gathered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81b61c98-839a-488b-a0da-085f8891197c">get_Phone</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that fired this event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd43ce66-bcbf-4863-87cc-db10dd81ba99">get_RingMode</a>
</td>
<td align="left" width="63%">
Gets a long value specifying the ring mode to which the phone has transitioned.

</td>
</tr>
</table> 

