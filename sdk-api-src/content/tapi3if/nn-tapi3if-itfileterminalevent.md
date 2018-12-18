---
UID: NN:tapi3if.ITFileTerminalEvent
title: ITFileTerminalEvent
author: windows-sdk-content
description: The ITFileTerminalEvent interface contains methods that retrieve the description of file terminal events that have occurred.
old-location: tapi3\itfileterminalevent.htm
tech.root: tapi
ms.assetid: cb6f2869-ec31-49ac-873b-35a0dcd2c8d7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITFileTerminalEvent, ITFileTerminalEvent interface [TAPI 2.2], ITFileTerminalEvent interface [TAPI 2.2],described, _tapi3_itfileterminalevent, tapi3.itfileterminalevent, tapi3if/ITFileTerminalEvent
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
 - ITFileTerminalEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTerminalEvent interface


## -description


The 
<b>ITFileTerminalEvent</b> interface contains methods that retrieve the description of file terminal events that have occurred. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_FILETERMINAL</b>, the method's <i>pEvent</i> parameter is an 
<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> pointer for the 
<b>ITFileTerminalEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_FILETERMINAL</b> to enable reception of file terminal events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITFileTerminalEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITFileTerminalEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITFileTerminalEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a9745a7-8119-41a0-b09a-3475f2390d4d">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the call information interface for the call on which the event has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90594778-712e-4d26-9fe5-cb5cfd240359">get_Cause</a>
</td>
<td align="left" width="63%">
Gets the cause associated with this event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eabd161-12d1-4537-beb1-3a05996aa506">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error code for the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f75537e8-f54c-4165-ba89-013eeabceb74">get_State</a>
</td>
<td align="left" width="63%">
Gets the new file terminal state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/515d9c65-1c24-485a-b7e4-1640e4e8c382">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets the file terminal that generated this event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f860faf3-6ca5-43d3-8d68-487d1b1d29b0">get_Track</a>
</td>
<td align="left" width="63%">
Gets the track terminal that generated this event.

</td>
</tr>
</table> 

