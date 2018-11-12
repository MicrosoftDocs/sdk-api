---
UID: NN:tapi3.ITQueueEvent
title: ITQueueEvent
author: windows-sdk-content
description: The ITQueueEvent interface contains methods that retrieve the description of Automatic Call Distribution (ACD) queue events.
old-location: tapi3\itqueueevent.htm
tech.root: tapi
ms.assetid: 7e4655ff-6ed4-4166-91f7-49d2e0556662
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITQueueEvent, ITQueueEvent interface [TAPI 2.2], ITQueueEvent interface [TAPI 2.2],described, _tapi3_itqueueevent, tapi3.itqueueevent, tapi3cc/ITQueueEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3.h
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
 - ITQueueEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITQueueEvent interface


## -description


The 
<b>ITQueueEvent</b> interface contains methods that retrieve the description of Automatic Call Distribution (ACD) queue events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_QUEUE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITQueueEvent</b> interface. The methods of this interface can be used to retrieve information concerning a queue event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_QUEUE</b> event to enable reception of ACD queue events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITQueueEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITQueueEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITQueueEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/704a9601-e8c3-42d4-86bc-be59c44a05b3">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/5a2efb70-a943-46c5-a362-18579ad8c965">ACDQUEUE_EVENT</a> descriptor of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59a4be82-0118-4a9c-9f85-0febfe1b3e18">get_Queue</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5a2efb70-a943-46c5-a362-18579ad8c965">ACDQUEUE_EVENT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

