---
UID: NN:tapi3if.ITASRTerminalEvent
title: ITASRTerminalEvent
author: windows-sdk-content
description: The ITASRTerminalEvent interface contains methods that retrieve the description of Automatic Speech Recognition terminal events that have occurred.
old-location: tapi3\itasrterminalevent.htm
tech.root: tapi
ms.assetid: 6bf8b1b7-698f-443f-9ddf-0d50551cebab
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITASRTerminalEvent, ITASRTerminalEvent interface [TAPI 2.2], ITASRTerminalEvent interface [TAPI 2.2],described, _tapi3_itasrterminalevent, tapi3.itasrterminalevent, tapi3if/ITASRTerminalEvent
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
 - ITASRTerminalEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITASRTerminalEvent interface


## -description


The 
<b>ITASRTerminalEvent</b> interface contains methods that retrieve the description of Automatic Speech Recognition terminal events that have occurred. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_ASRTERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer for the 
<b>ITASRTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_ASRTERMINAL</b> to enable reception of Automatic Speech Recognition terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITASRTerminalEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITASRTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITASRTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8736e3bc-9f79-4b0f-84a7-00e6d20550e2">get_Call</a>
</td>
<td align="left" width="63%">
Returns a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call object involved in the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bccf537-a54b-4c40-866b-0f7a42149841">get_Error</a>
</td>
<td align="left" width="63%">
Returns an HRESULT cast of the error associated with the terminal event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cde7b16-f825-4591-9947-6ad03cbd14c6">get_Terminal</a>
</td>
<td align="left" width="63%">
Returns a pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface for the terminal on which the event occurred.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

