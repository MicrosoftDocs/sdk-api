---
UID: NN:strmif.IAMTimecodeDisplay
title: IAMTimecodeDisplay (strmif.h)
description: The IAMTimecodeDisplay interface controls an external SMPTE/MIDI timecode display device.DirectShow currently does not provide any filters that implement this interface.
helpviewer_keywords: ["IAMTimecodeDisplay","IAMTimecodeDisplay interface [DirectShow]","IAMTimecodeDisplay interface [DirectShow]","described","IAMTimecodeDisplayInterface","dshow.iamtimecodedisplay","strmif/IAMTimecodeDisplay"]
old-location: dshow\iamtimecodedisplay.htm
tech.root: dshow
ms.assetid: 2edfc260-5bb6-475d-b8af-252e7c7a8552
ms.date: 12/05/2018
ms.keywords: IAMTimecodeDisplay, IAMTimecodeDisplay interface [DirectShow], IAMTimecodeDisplay interface [DirectShow],described, IAMTimecodeDisplayInterface, dshow.iamtimecodedisplay, strmif/IAMTimecodeDisplay
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTimecodeDisplay
 - strmif/IAMTimecodeDisplay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeDisplay
---

# IAMTimecodeDisplay interface


## -description

The <code>IAMTimecodeDisplay</code> interface controls an external SMPTE/MIDI timecode display device.

DirectShow currently does not provide any filters that implement this interface. Third parties should implement this interface on any filter that controls the timecode display of an external timecode reader or generator. Timecode readers or generators can be built into a VCR or can be separate external devices.

This interface is not intended for rendering in a DirectShow filter graph; it is purely for use on external device displays.

<b>Hardware Requirements</b>

See the <a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a> interface for hardware requirements.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeDisplay</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTimecodeDisplay</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTimecodeDisplay</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-gettcdisplay">GetTCDisplay</a>
</td>
<td align="left" width="63%">
Retrieves current settings of the timecode character generator output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-gettcdisplayenable">GetTCDisplayEnable</a>
</td>
<td align="left" width="63%">
Determines whether an external device's timecode character generator output is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-settcdisplay">SetTCDisplay</a>
</td>
<td align="left" width="63%">
Sets the timecode character generator output characteristics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-settcdisplayenable">SetTCDisplayEnable</a>
</td>
<td align="left" width="63%">
Enables or disables an external device's timecode character output generator.

</td>
</tr>
</table>