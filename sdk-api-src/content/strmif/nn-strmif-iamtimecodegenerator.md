---
UID: NN:strmif.IAMTimecodeGenerator
title: IAMTimecodeGenerator (strmif.h)
description: The IAMTimecodeGenerator interface controls how an external SMPTE/MIDI timecode generator supplies data to the filter graph.DirectShow currently does not provide any filters that implement this interface.
old-location: dshow\iamtimecodegenerator.htm
tech.root: DirectShow
ms.assetid: 7fe74fc2-03bd-43dd-917f-ee0149f1e17f
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator, IAMTimecodeGenerator interface [DirectShow], IAMTimecodeGenerator interface [DirectShow],described, IAMTimecodeGeneratorInterface, dshow.iamtimecodegenerator, strmif/IAMTimecodeGenerator
ms.topic: interface
f1_keywords:
- strmif/IAMTimecodeGenerator
dev_langs:
- c++
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

Optionally, you can enable applications to convert timecode to reference time by supporting the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-converttimeformat">IMediaSeeking::ConvertTimeFormat</a> method on the filter.

<b>Hardware Requirements</b>

For hardware requirements, see the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTimecodeGenerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTimecodeGenerator</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-get_vitcline">get_VITCLine</a>
</td>
<td align="left" width="63%">
Retrieves which line(s) the vertical interval timecode information has been inserted into.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-gettcgmode">GetTCGMode</a>
</td>
<td align="left" width="63%">
Retrieves the SMPTE timecode generator properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-gettimecode">GetTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the most recent timecode and/or userbit value available in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-put_vitcline">put_VITCLine</a>
</td>
<td align="left" width="63%">
Specifies which line(s) to insert the vertical interval timecode information into.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-settcgmode">SetTCGMode</a>
</td>
<td align="left" width="63%">
Sets the SMPTE timecode generator properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-settimecode">SetTimecode</a>
</td>
<td align="left" width="63%">
Sets the timecode, userbit value, or both.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>
 

 

