---
UID: NN:tapi3if.ITDigitGenerationEvent
title: ITDigitGenerationEvent
author: windows-sdk-content
description: The ITDigitGenerationEvent interface contains methods that describe digit generation events.
old-location: tapi3\itdigitgenerationevent.htm
tech.root: Tapi
ms.assetid: 788eee9c-b885-4b94-b259-694353c0f63a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITDigitGenerationEvent, ITDigitGenerationEvent interface [TAPI 2.2], ITDigitGenerationEvent interface [TAPI 2.2],described, _tapi3_itdigitgenerationevent, tapi3.itdigitgenerationevent, tapi3if/ITDigitGenerationEvent
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
 - ITDigitGenerationEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitGenerationEvent interface


## -description


The 
<b>ITDigitGenerationEvent</b> interface contains methods that describe digit generation events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_GENERATEEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITDigitGenerationEvent</b> interface. The methods of this interface can be used to report on calls that require the generation of DTMF digits. This interface is implemented by the application and called by the TAPI 3 DLL.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_GENERATEEVENT</b> event to enable reception of digit generation events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDigitGenerationEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITDigitGenerationEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDigitGenerationEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f4281f-e1df-4be9-acfc-5482044eb44b">get_Call</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0cc1e75-bdc2-4b05-a83b-13e4778ed75b">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70e8c932-a157-455e-b340-d7e4eb19823c">get_GenerationTermination</a>
</td>
<td align="left" width="63%">
Gets the digit or digits that indicate the end of the generated digit series.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daae0ae5-0eaf-4ca7-b08a-1c46b9ebfcab">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which the digit-gathering completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>
 

 

