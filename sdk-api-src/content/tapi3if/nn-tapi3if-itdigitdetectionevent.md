---
UID: NN:tapi3if.ITDigitDetectionEvent
title: ITDigitDetectionEvent
author: windows-sdk-content
description: The ITDigitDetectionEvent interface contains methods that retrieve the description of DTMF digit events.
old-location: tapi3\itdigitdetectionevent.htm
tech.root: TAPI
ms.assetid: f387f5f5-06e4-45f2-8d93-31ff0da6151a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITDigitDetectionEvent, ITDigitDetectionEvent interface [TAPI 2.2], ITDigitDetectionEvent interface [TAPI 2.2],described, _tapi3_itdigitdetectionevent, tapi3.itdigitdetectionevent, tapi3if/ITDigitDetectionEvent
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
 - ITDigitDetectionEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitDetectionEvent interface


## -description


The 
<b>ITDigitDetectionEvent</b> interface contains methods that retrieve the description of DTMF digit events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_DIGITEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITDigitDetectionEvent</b> interface. The methods of this interface can be used to detect DTMF digits during a call. This interface is implemented by the application and called by the TAPI 3 DLL.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_DIGITEVENT</b> event to enable reception of DTMF digit events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. You must also call <a href="https://msdn.microsoft.com/09adb3fb-cf77-4c8b-beab-85d173cbb242">ITLegacyCallMediaControl::DetectDigits</a> to indicate which type of digit detection is needed. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDigitDetectionEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITDigitDetectionEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDigitDetectionEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98168b0c-132b-47cf-9d5d-6fba7b570216">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e24d6a37-8f72-42d7-8162-b201eed3cc9a">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b62418de-9a3e-46f1-88d9-7e147859ec96">get_Digit</a>
</td>
<td align="left" width="63%">
Gets a digit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7eeda641-9155-4628-b4b2-2d427a255d7c">get_DigitMode</a>
</td>
<td align="left" width="63%">
Gets the descriptor of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">line digit mode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24c83763-366b-4e1b-8662-9d87250b7945">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which the digit-gathering completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code
		  snippet</a>
 

 

