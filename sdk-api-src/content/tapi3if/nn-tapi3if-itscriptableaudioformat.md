---
UID: NN:tapi3if.ITScriptableAudioFormat
title: ITScriptableAudioFormat (tapi3if.h)
description: The ITScriptableAudioFormat interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the WAVEFORMATEX structure.
helpviewer_keywords: ["ITScriptableAudioFormat","ITScriptableAudioFormat interface [TAPI 2.2]","ITScriptableAudioFormat interface [TAPI 2.2]","described","_tapi3_itscriptableaudioformat","tapi3.itscriptableaudioformat","tapi3if/ITScriptableAudioFormat"]
old-location: tapi3\itscriptableaudioformat.htm
tech.root: Tapi
ms.assetid: 6b5d069a-044f-4bd4-b661-6100a2607107
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat, ITScriptableAudioFormat interface [TAPI 2.2], ITScriptableAudioFormat interface [TAPI 2.2],described, _tapi3_itscriptableaudioformat, tapi3.itscriptableaudioformat, tapi3if/ITScriptableAudioFormat
f1_keywords:
- tapi3if/ITScriptableAudioFormat
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
- ITScriptableAudioFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITScriptableAudioFormat interface


## -description


The 
<b>ITScriptableAudioFormat</b> interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the 
<a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_audioformatforscripting">ITFileTrack::get_AudioFormatForScripting</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itfiletrack-get_emptyaudioformatforscripting">ITFileTrack::get_EmptyAudioFormatForScripting</a> methods create the 
<b>ITScriptableAudioFormat</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITScriptableAudioFormat</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITScriptableAudioFormat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITScriptableAudioFormat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_avgbytespersec">get_AvgBytesPerSec</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nAvgBytesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_bitspersample">get_BitsPerSample</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>wBitsPerSample</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_blockalign">get_BlockAlign</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nBlockAlign</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_channels">get_Channels</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nChannels</b> member in the 
<a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_formattag">get_FormatTag</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>wFormatTag</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_samplespersec">get_SamplesPerSec</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nSamplesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_avgbytespersec">put_AvgBytesPerSec</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nAvgBytesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_bitspersample">put_BitsPerSample</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>wBitsPerSample</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_blockalign">put_BlockAlign</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nBlockAlign</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_channels">put_Channels</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nChannels</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_formattag">put_FormatTag</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>wFormatTag</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_samplespersec">put_SamplesPerSec</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>nSamplesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
</table> 

