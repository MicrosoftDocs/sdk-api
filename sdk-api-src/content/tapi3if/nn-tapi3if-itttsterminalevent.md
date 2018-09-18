---
UID: NN:tapi3if.ITTTSTerminalEvent
title: ITTTSTerminalEvent
author: windows-sdk-content
description: The ITTTSTerminalEvent interface contains methods that retrieve the description of Text-to-Speech (TTS) terminal events that have occurred.
old-location: tapi3\itttsterminalevent.htm
tech.root: TAPI
ms.assetid: 0375d6e4-cd9f-4245-abf5-1b200af79848
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITTTSTerminalEvent, ITTTSTerminalEvent interface [TAPI 2.2], ITTTSTerminalEvent interface [TAPI 2.2],described, _tapi3_itttsterminalevent, tapi3.itttsterminalevent, tapi3if/ITTTSTerminalEvent
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
 - ITTTSTerminalEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTTSTerminalEvent interface


## -description


The 
<b>ITTTSTerminalEvent</b> interface contains methods that retrieve the description of Text-to-Speech (TTS) terminal events that have occurred.

When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_TTSTERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer for the 
<b>ITTTSTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_TTSTERMINAL</b> to enable reception of Text-to-Speech terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTTSTerminalEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITTTSTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTTSTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e9ffff3-1282-4d05-83c9-7f824406fcfa">get_Call</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface pointer for the call object involved in the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a120114-a902-4e66-81e5-9f10205714ad">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error code involved in the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce37e074-8ce0-4fde-b16a-c85a9487f0db">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointer for the terminal object involved in the terminal event.

</td>
</tr>
</table> 

