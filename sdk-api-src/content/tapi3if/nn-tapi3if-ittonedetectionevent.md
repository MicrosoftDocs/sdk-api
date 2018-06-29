---
UID: NN:tapi3if.ITToneDetectionEvent
title: ITToneDetectionEvent
author: windows-sdk-content
description: The ITToneDetectionEvent interface exposes methods that allow an application to retrieve information about a tone detection event.
old-location: tapi3\ittonedetectionevent.htm
old-project: Tapi
ms.assetid: 1e0f71a2-1aae-46b7-9147-7bf9da4d9503
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITToneDetectionEvent, ITToneDetectionEvent interface [TAPI 2.2], ITToneDetectionEvent interface [TAPI 2.2],described, _tapi3_ittonedetectionevent, tapi3.ittonedetectionevent, tapi3if/ITToneDetectionEvent
ms.prod: windows
ms.technology: windows-sdk
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
 - ITToneDetectionEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITToneDetectionEvent interface


## -description


The 
<b>ITToneDetectionEvent</b> interface exposes methods that allow an application to retrieve information about a tone detection event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITToneDetectionEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITToneDetectionEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5c6c4890-7e65-4b4a-bc2f-ea3c11e5e85a">get_AppSpecific</a>
</td>
<td align="left" width="63%">
Gets the application-defined tag that identifies the tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50804e3d-ec60-44b3-ac6d-2518c96bfc64">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ebd7fae-0060-4937-9812-8b48eceb9139">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets a pointer to the application's callback function that will process the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01a00b2c-d4b0-4de0-91b8-0741ed1fd300">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which the tone was detected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19e82bf6-63e9-45e2-8ba8-7924bbf02fb6">get_ToneListID</a>
</td>
<td align="left" width="63%">
Gets the tone list ID for the tone that was detected.

</td>
</tr>
</table> 

