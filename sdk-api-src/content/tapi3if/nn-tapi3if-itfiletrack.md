---
UID: NN:tapi3if.ITFileTrack
title: ITFileTrack (tapi3if.h)
author: windows-sdk-content
description: The ITFileTrack interface exposes methods that allow an application to get and set information concerning file terminal tracks. The ITFileTerminalEvent::get_Track method creates the ITFileTrack interface.
old-location: tapi3\itfiletrack.htm
tech.root: Tapi
ms.assetid: 590ca1ea-e058-4238-b01c-249fddd3c87d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITFileTrack, ITFileTrack interface [TAPI 2.2], ITFileTrack interface [TAPI 2.2],described, _tapi3_itfiletrack, tapi3.itfiletrack, tapi3if/ITFileTrack
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITFileTrack"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITFileTrack interface


## -description


The 
<b>ITFileTrack</b> interface exposes methods that allow an application to get and set information concerning file terminal tracks. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfileterminalevent-get_track">ITFileTerminalEvent::get_Track</a> method creates the 
<b>ITFileTrack</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITFileTrack</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITFileTrack</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_audioformatforscripting">get_AudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Gets the audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_controllingterminal">get_ControllingTerminal</a>
</td>
<td align="left" width="63%">
Gets the multitrack terminal that controls the current track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_emptyaudioformatforscripting">get_EmptyAudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Gets an empty audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_format">get_Format</a>
</td>
<td align="left" width="63%">
Gets the file terminal's format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-put_audioformatforscripting">put_AudioFormatForScripting</a>
</td>
<td align="left" width="63%">
Sets the audio scripting format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-put_format">put_Format</a>
</td>
<td align="left" width="63%">
Sets the file terminal's format.

</td>
</tr>
</table> 

