---
UID: NN:tapi3if.ITCallHubEvent
title: ITCallHubEvent
author: windows-sdk-content
description: The ITCallHubEvent interface contains methods that retrieve the description of CallHub events.
old-location: tapi3\itcallhubevent.htm
tech.root: tapi
ms.assetid: 4008fc7e-f095-442d-9214-61bfead8cf04
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallHubEvent, ITCallHubEvent interface [TAPI 2.2], ITCallHubEvent interface [TAPI 2.2],described, _tapi3_itcallhubevent, tapi3.itcallhubevent, tapi3if/ITCallHubEvent
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
 - ITCallHubEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallHubEvent interface


## -description


The 
<b>ITCallHubEvent</b> interface contains methods that retrieve the description of CallHub events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_CALLHUB</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallHubEvent</b> interface. The methods of this interface can be used to retrieve information concerning the CallHub change that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLHUB</b> event to enable reception of CallHub events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallHubEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITCallHubEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallHubEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ac47da3-f60f-41f4-99f7-031744044bd4">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4016f253-2a2d-4406-a1fc-7595d25c1c06">get_CallHub</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2515583-e564-413d-b93f-6f2dd7776d7b">get_Event</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://msdn.microsoft.com/199e6c8b-805c-40c6-80d0-2e5803ec85a1">CALLHUB_EVENT</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/199e6c8b-805c-40c6-80d0-2e5803ec85a1">CALLHUB_EVENT</a>



<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

