---
UID: NN:strmif.IAMTimecodeDisplay
title: IAMTimecodeDisplay
author: windows-sdk-content
description: The IAMTimecodeDisplay interface controls an external SMPTE/MIDI timecode display device.DirectShow currently does not provide any filters that implement this interface.
old-location: dshow\iamtimecodedisplay.htm
old-project: DirectShow
ms.assetid: 2edfc260-5bb6-475d-b8af-252e7c7a8552
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMTimecodeDisplay, IAMTimecodeDisplay interface [DirectShow], IAMTimecodeDisplay interface [DirectShow],described, IAMTimecodeDisplayInterface, dshow.iamtimecodedisplay, strmif/IAMTimecodeDisplay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTimecodeDisplay
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeDisplay interface


## -description



The <code>IAMTimecodeDisplay</code> interface controls an external SMPTE/MIDI timecode display device.

DirectShow currently does not provide any filters that implement this interface. Third parties should implement this interface on any filter that controls the timecode display of an external timecode reader or generator. Timecode readers or generators can be built into a VCR or can be separate external devices.

This interface is not intended for rendering in a DirectShow filter graph; it is purely for use on external device displays.

<b>Hardware Requirements</b>

See the <a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport</a> interface for hardware requirements.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeDisplay</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMTimecodeDisplay</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3da33500-1b1d-4818-b69b-74f302614349">GetTCDisplay</a>
</td>
<td align="left" width="63%">
Retrieves current settings of the timecode character generator output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe8bac4d-a271-47b3-9737-f115429b50aa">GetTCDisplayEnable</a>
</td>
<td align="left" width="63%">
Determines whether an external device's timecode character generator output is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34d55c5a-d213-4fb2-b81c-b117d025f3ec">SetTCDisplay</a>
</td>
<td align="left" width="63%">
Sets the timecode character generator output characteristics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae4eeeaa-1c73-4e3a-82b1-a073d9c7d667">SetTCDisplayEnable</a>
</td>
<td align="left" width="63%">
Enables or disables an external device's timecode character output generator.

</td>
</tr>
</table> 

