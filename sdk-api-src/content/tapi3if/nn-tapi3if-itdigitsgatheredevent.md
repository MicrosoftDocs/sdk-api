---
UID: NN:tapi3if.ITDigitsGatheredEvent
title: ITDigitsGatheredEvent (tapi3if.h)
description: The ITDigitsGatheredEvent interface exposes methods that allow an application to retrieve data when the TAPI Server sends an event indicating that the Server has gathered digits required by the application.
helpviewer_keywords: ["ITDigitsGatheredEvent","ITDigitsGatheredEvent interface [TAPI 2.2]","ITDigitsGatheredEvent interface [TAPI 2.2]","described","_tapi3_itdigitsgatheredevent","tapi3.itdigitsgatheredevent","tapi3if/ITDigitsGatheredEvent"]
old-location: tapi3\itdigitsgatheredevent.htm
tech.root: tapi3
ms.assetid: 2d710bea-a0fd-492b-81a3-03b741685c91
ms.date: 12/05/2018
ms.keywords: ITDigitsGatheredEvent, ITDigitsGatheredEvent interface [TAPI 2.2], ITDigitsGatheredEvent interface [TAPI 2.2],described, _tapi3_itdigitsgatheredevent, tapi3.itdigitsgatheredevent, tapi3if/ITDigitsGatheredEvent
f1_keywords:
- tapi3if/ITDigitsGatheredEvent
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDigitsGatheredEvent interface


## -description


The 
<b>ITDigitsGatheredEvent</b> interface exposes methods that allow an application to retrieve data when the TAPI Server sends an event indicating that the Server has gathered digits required by the application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDigitsGatheredEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDigitsGatheredEvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_callbackinstance">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets a pointer to the application's callback function that will process the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_digits">get_Digits</a>
</td>
<td align="left" width="63%">
Gets the gathered digits for the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_gathertermination">get_GatherTermination</a>
</td>
<td align="left" width="63%">
Gets the reason why digit-gathering was terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_tickcount">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which digit-gathering completed.

</td>
</tr>
</table> 

