---
UID: NN:tapi3if.ITFileTrack
title: ITFileTrack
author: windows-sdk-content
description: The ITFileTrack interface exposes methods that allow an application to get and set information concerning file terminal tracks. The ITFileTerminalEvent::get_Track method creates the ITFileTrack interface.
old-location: tapi3\itfiletrack.htm
tech.root: TAPI
ms.assetid: 590ca1ea-e058-4238-b01c-249fddd3c87d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITFileTrack, ITFileTrack interface [TAPI 2.2], ITFileTrack interface [TAPI 2.2],described, _tapi3_itfiletrack, tapi3.itfiletrack, tapi3if/ITFileTrack
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
 - ITFileTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTrack interface


## -description


The 
<b>ITFileTrack</b> interface exposes methods that allow an application to get and set information concerning file terminal tracks. The 
<a href="https://msdn.microsoft.com/f860faf3-6ca5-43d3-8d68-487d1b1d29b0">ITFileTerminalEvent::get_Track</a> method creates the 
<b>ITFileTrack</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITFileTrack</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITFileTrack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITFileTrack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3677b85c-15a4-4960-88ad-18855349fedd">get_AudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Gets the audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3a2c5e7-0134-4dad-b192-7a6c71dabe54">get_ControllingTerminal</a>
</td>
<td align="left" width="63%">
Gets the multitrack terminal that controls the current track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80644b51-4b04-4299-a486-284e77583feb">get_EmptyAudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Gets an empty audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d489888-49b3-4fcd-9643-82f0a08fe1c6">get_Format</a>
</td>
<td align="left" width="63%">
Gets the file terminal's format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ec8ede-8801-418d-9264-415b78abb336">put_AudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Sets the audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a60e3f-d310-457d-8d1b-17860165c1e9">put_Format</a>
</td>
<td align="left" width="63%">
Sets the file terminal's format.

</td>
</tr>
</table> 

