---
UID: NN:tapi3if.ITCallInfoChangeEvent
title: ITCallInfoChangeEvent
author: windows-sdk-content
description: The ITCallInfoChangeEvent interface contains methods that retrieve the description of call information change events.
old-location: tapi3\itcallinfochangeevent.htm
old-project: tapi
ms.assetid: f543da95-c0cc-4631-b91e-ba02dde2c081
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallInfoChangeEvent, ITCallInfoChangeEvent interface [TAPI 2.2], ITCallInfoChangeEvent interface [TAPI 2.2],described, _tapi3_itcallinfochangeevent, tapi3.itcallinfochangeevent, tapi3if/ITCallInfoChangeEvent
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
 - ITCallInfoChangeEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallInfoChangeEvent interface


## -description


The 
<b>ITCallInfoChangeEvent</b> interface contains methods that retrieve the description of call information change events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_CALLINFOCHANGE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallInfoChangeEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call information that has changed.

The 
<b>ITCallInfoChangeEvent</b> is an outgoing interface. This interface is registered with the TAPI object to get all information about calls. An application must have called the 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> method on the TAPI object before registering this interface. If not, the call to <b>Advise</b> will fail. This interface cannot be unregistered—<b>Unadvise</b> will always fail.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLINFOCHANGE</b> event to enable reception of call information change events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallInfoChangeEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITCallInfoChangeEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallInfoChangeEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee6c4f2f-e53c-4eae-b86c-2849395cca74">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feb9fbcd-58e6-48c7-ab21-9ba0fd766b25">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c49a5624-8867-46c0-acf6-5e60667fc969">get_Cause</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/587329e2-3b5f-4d9e-9cec-2676c0bd1de8">CALLINFOCHANGE_CAUSE</a> descriptor of the change.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

