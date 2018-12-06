---
UID: NN:tapi3if.ITDigitsGatheredEvent
title: ITDigitsGatheredEvent
author: windows-sdk-content
description: The ITDigitsGatheredEvent interface exposes methods that allow an application to retrieve data when the TAPI Server sends an event indicating that the Server has gathered digits required by the application.
old-location: tapi3\itdigitsgatheredevent.htm
tech.root: tapi
ms.assetid: 2d710bea-a0fd-492b-81a3-03b741685c91
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITDigitsGatheredEvent, ITDigitsGatheredEvent interface [TAPI 2.2], ITDigitsGatheredEvent interface [TAPI 2.2],described, _tapi3_itdigitsgatheredevent, tapi3.itdigitsgatheredevent, tapi3if/ITDigitsGatheredEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3if.h
req.include-header: 
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
 - ITDigitsGatheredEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitsGatheredEvent interface


## -description


The 
<b>ITDigitsGatheredEvent</b> interface exposes methods that allow an application to retrieve data when the TAPI Server sends an event indicating that the Server has gathered digits required by the application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDigitsGatheredEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITDigitsGatheredEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDigitsGatheredEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43625f93-4ab2-4aeb-83da-70310f118e34">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28c613bc-8320-43b5-a9b3-b6a47876d7dd">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets a pointer to the application's callback function that will process the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/940e186b-33bd-4846-8314-39ede19bad95">get_Digits</a>
</td>
<td align="left" width="63%">
Gets the gathered digits for the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97c123b9-4497-43f3-b747-660d3f9f5848">get_GatherTermination</a>
</td>
<td align="left" width="63%">
Gets the reason why digit-gathering was terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e5fbed0-f132-418f-aa71-36d0e673affa">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which digit-gathering completed.

</td>
</tr>
</table> 

