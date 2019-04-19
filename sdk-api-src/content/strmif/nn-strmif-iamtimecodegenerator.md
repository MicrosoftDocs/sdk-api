---
UID: NN:strmif.IAMTimecodeGenerator
title: IAMTimecodeGenerator (strmif.h)
author: windows-sdk-content
description: The IAMTimecodeGenerator interface controls how an external SMPTE/MIDI timecode generator supplies data to the filter graph.DirectShow currently does not provide any filters that implement this interface.
old-location: dshow\iamtimecodegenerator.htm
tech.root: DirectShow
ms.assetid: 7fe74fc2-03bd-43dd-917f-ee0149f1e17f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator, IAMTimecodeGenerator interface [DirectShow], IAMTimecodeGenerator interface [DirectShow],described, IAMTimecodeGeneratorInterface, dshow.iamtimecodegenerator, strmif/IAMTimecodeGenerator
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeGenerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeGenerator interface


## -description



The <code>IAMTimecodeGenerator</code> interface controls how an external SMPTE/MIDI timecode generator supplies data to the filter graph.

DirectShow currently does not provide any filters that implement this interface. Third parties should implement this interface on any filter that controls an external timecode generator. Timecode generators can be built into a VCR or can be separate external devices. The device must be able to read timecode and send it to the computer over its control interface. If not, the user must have a timecode reader card in the computer, or you can write a software decoder that converts VITC embedded in captured video frames or LTC captured as an audio signal into DirectShow timecode samples.

SMPTE timecode is a frame addressing system that identifies video and audio sources, makes automatic track synchronization possible, and provides a container for additional data related to the production. SMPTE timecode's main purpose is to provide a machine-readable address for video and audio. It is displayed in hh:mm:ss:ff format and is thoroughly defined in ANSI/SMPTE 12-1986.

Optionally, you can enable applications to convert timecode to reference time by supporting the <a href="https://msdn.microsoft.com/868ec03e-d4e5-4a1e-914a-6be8933f1c7c">IMediaSeeking::ConvertTimeFormat</a> method on the filter.

<b>Hardware Requirements</b>

For hardware requirements, see the <a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeGenerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMTimecodeGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTimecodeGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a1595a6-30ae-46ab-bfda-102b4dbc67ef">get_VITCLine</a>
</td>
<td align="left" width="63%">
Retrieves which line(s) the vertical interval timecode information has been inserted into.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a754e3-4071-437a-bd98-99a94e2594a3">GetTCGMode</a>
</td>
<td align="left" width="63%">
Retrieves the SMPTE timecode generator properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f24a99-5a6b-4aff-b22c-e05811c910f4">GetTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the most recent timecode and/or userbit value available in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351bf80b-f14c-454f-9d20-ceff4a437fcd">put_VITCLine</a>
</td>
<td align="left" width="63%">
Specifies which line(s) to insert the vertical interval timecode information into.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61434534-0a43-4bf3-81d1-3b27ac601cb4">SetTCGMode</a>
</td>
<td align="left" width="63%">
Sets the SMPTE timecode generator properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6da4b7e0-e6cd-4555-b5a3-e5f0f20ff070">SetTimecode</a>
</td>
<td align="left" width="63%">
Sets the timecode, userbit value, or both.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>
 

 

