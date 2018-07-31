---
UID: NN:tapi3if.ITToneTerminalEvent
title: ITToneTerminalEvent
author: windows-sdk-content
description: The ITToneTerminalEvent interface contains methods that retrieve the description of tone terminal events that have occurred.
old-location: tapi3\ittoneterminalevent.htm
old-project: Tapi
ms.assetid: 6a5d03e9-e6d1-452a-a189-ca693a72c610
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITToneTerminalEvent, ITToneTerminalEvent interface [TAPI 2.2], ITToneTerminalEvent interface [TAPI 2.2],described, _tapi3_ittoneterminalevent, tapi3.ittoneterminalevent, tapi3if/ITToneTerminalEvent
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
 - ITToneTerminalEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITToneTerminalEvent interface


## -description


The 
<b>ITToneTerminalEvent</b> interface contains methods that retrieve the description of tone terminal events that have occurred.

When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_TONETERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer for the 
<b>ITToneTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_TONETERMINAL</b> to enable reception of tone terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITToneTerminalEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITToneTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITToneTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adbbce76-827d-439c-865d-9dcfe40c9722">get_Call</a>
</td>
<td align="left" width="63%">
Gets the call on which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f91497b0-b340-4eb9-8d9f-364991343c3b">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error code involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3358e219-fde9-4b60-bf75-c6d8c42a51ea">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets the terminal on which the event occurred.

</td>
</tr>
</table> 

