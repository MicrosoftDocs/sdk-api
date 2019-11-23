---
UID: NN:tapi3if.ITToneDetectionEvent
title: ITToneDetectionEvent (tapi3if.h)

description: The ITToneDetectionEvent interface exposes methods that allow an application to retrieve information about a tone detection event.
old-location: tapi3\ittonedetectionevent.htm
tech.root: Tapi
ms.assetid: 1e0f71a2-1aae-46b7-9147-7bf9da4d9503

ms.date: 12/05/2018
ms.keywords: ITToneDetectionEvent, ITToneDetectionEvent interface [TAPI 2.2], ITToneDetectionEvent interface [TAPI 2.2],described, _tapi3_ittonedetectionevent, tapi3.ittonedetectionevent, tapi3if/ITToneDetectionEvent
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITToneDetectionEvent"
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
 - ITToneDetectionEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITToneDetectionEvent interface


## -description


The 
<b>ITToneDetectionEvent</b> interface exposes methods that allow an application to retrieve information about a tone detection event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITToneDetectionEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITToneDetectionEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITToneDetectionEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittonedetectionevent-get_appspecific">get_AppSpecific</a>
</td>
<td align="left" width="63%">
Gets the application-defined tag that identifies the tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittonedetectionevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittonedetectionevent-get_callbackinstance">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets a pointer to the application's callback function that will process the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittonedetectionevent-get_tickcount">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which the tone was detected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms733258(v=vs.85)">get_ToneListID</a>
</td>
<td align="left" width="63%">
Gets the tone list ID for the tone that was detected.

</td>
</tr>
</table> 

