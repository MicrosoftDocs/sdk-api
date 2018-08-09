---
UID: NN:tapi3if.ITCallNotificationEvent
title: ITCallNotificationEvent
author: windows-sdk-content
description: The ITCallNotificationEvent interface contains methods that retrieve the description of call notification events.
old-location: tapi3\itcallnotificationevent.htm
old-project: tapi
ms.assetid: d0ea4f7a-7b50-4610-ae17-957c0c1891e1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallNotificationEvent, ITCallNotificationEvent interface [TAPI 2.2], ITCallNotificationEvent interface [TAPI 2.2],described, _tapi3_itcallnotificationevent, tapi3.itcallnotificationevent, tapi3if/ITCallNotificationEvent
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
 - ITCallNotificationEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallNotificationEvent interface


## -description


The 
<b>ITCallNotificationEvent</b> interface contains methods that retrieve the description of call notification events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_CALLNOTIFICATION</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallNotificationEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call notification event that has occurred.

This outgoing interface is registered with the TAPI object to get all information about calls. An application must call the 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> method on the TAPI object before registering this interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLNOTIFICATION</b> event to enable reception of call notification events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallNotificationEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITCallNotificationEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallNotificationEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ff82bd1-de69-4ab7-9152-a578b8566755">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daa6d980-49aa-4e5a-9871-77e39dcdb6f0">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08a3925c-e14e-442e-952e-483fc41d049c">get_Event</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

