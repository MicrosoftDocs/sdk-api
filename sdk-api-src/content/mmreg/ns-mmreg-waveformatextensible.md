---
UID: NS:mmreg.WAVEFORMATEXTENSIBLE
title: WAVEFORMATEXTENSIBLE (mmreg.h)
description: The WAVEFORMATEXTENSIBLE structure defines the format of waveform-audio data for formats having more than two channels or higher sample resolutions than allowed by WAVEFORMATEX.
helpviewer_keywords: ["*LPWAVEFORMATIEEEFLOATEX","*LPWAVEFORMATPCMEX","*NPWAVEFORMATIEEEFLOATEX","*NPWAVEFORMATPCMEX","*PWAVEFORMATEXTENSIBLE","*PWAVEFORMATIEEEFLOATEX","*PWAVEFORMATPCMEX","PWAVEFORMATEXTENSIBLE","PWAVEFORMATEXTENSIBLE structure pointer [Windows Multimedia]","WAVEFORMATEXTENSIBLE","WAVEFORMATEXTENSIBLE structure [Windows Multimedia]","WAVEFORMATIEEEFLOATEX","WAVEFORMATPCMEX","_win32_WAVEFORMATEXTENSIBLE_str","mmreg/PWAVEFORMATEXTENSIBLE","mmreg/WAVEFORMATEXTENSIBLE","multimedia.waveformatextensible"]
old-location: multimedia\waveformatextensible.htm
tech.root: Multimedia
ms.assetid: 179d6c0c-ea80-4e9f-9e1b-43785f20cbd3
ms.date: 4/26/2023
ms.keywords: '*LPWAVEFORMATIEEEFLOATEX, *LPWAVEFORMATPCMEX, *NPWAVEFORMATIEEEFLOATEX, *NPWAVEFORMATPCMEX, *PWAVEFORMATEXTENSIBLE, *PWAVEFORMATIEEEFLOATEX, *PWAVEFORMATPCMEX, PWAVEFORMATEXTENSIBLE, PWAVEFORMATEXTENSIBLE structure pointer [Windows Multimedia], WAVEFORMATEXTENSIBLE, WAVEFORMATEXTENSIBLE structure [Windows Multimedia], WAVEFORMATIEEEFLOATEX, WAVEFORMATPCMEX, _win32_WAVEFORMATEXTENSIBLE_str, mmreg/PWAVEFORMATEXTENSIBLE, mmreg/WAVEFORMATEXTENSIBLE, multimedia.waveformatextensible'
req.header: mmreg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmreg/WAVEFORMATEXTENSIBLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmreg.h
api_name:
 - WAVEFORMATEXTENSIBLE
---

# WAVEFORMATEXTENSIBLE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WAVEFORMATEXTENSIBLE</b> structure defines the format of waveform-audio data for formats having more than two channels or higher sample resolutions than allowed by <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>. It can also be used to define any format that can be defined by <b>WAVEFORMATEX</b>.

## -struct-fields

### -field wFormatTag

### -field nChannels

### -field nSamplesPerSec

### -field nAvgBytesPerSec

### -field nBlockAlign

### -field wBitsPerSample

### -field cbSize

### -field wValidBitsPerSample

### -field dwChannelMask

Bitmask specifying the assignment of channels in the stream to speaker positions.

### -field SubFormat

Subformat of the data, such as KSDATAFORMAT_SUBTYPE_PCM. The subformat information is similar to that provided by the tag in the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure's <b>wFormatTag</b> member.

### -field Format

<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that specifies the basic format. The <b>wFormatTag</b> member must be WAVE_FORMAT_EXTENSIBLE. The <b>cbSize</b> member must be at least 22.

### -field Samples

A union describing the sample format.

### -field Samples.wValidBitsPerSample

Number of bits of precision in the signal. Usually equal to <b>WAVEFORMATEX.wBitsPerSample</b>. However, <b>wBitsPerSample</b> is the container size and must be a multiple of 8, whereas <b>wValidBitsPerSample</b> can be any value not exceeding the container size. For example, if the format uses 20-bit samples, <b>wBitsPerSample</b> must be at least 24, but <b>wValidBitsPerSample</b> is 20.

### -field Samples.wSamplesPerBlock

 
Number of samples contained in one compressed block of audio data. This value is used in buffer estimation. This value is used with compressed formats that have a fixed number of samples within each block. This value can be set to 0 if a variable number of samples is contained in each block of compressed audio data. In this case, buffer estimation and position information needs to be obtained in other ways.

### -field Samples.wReserved

Reserved for internal use by operating system. Set to 0.

## -remarks

<b>WAVEFORMATEXTENSIBLE</b> can describe any format that can be described by <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>, but provides additional support for more than two channels, for greater precision in the number of bits per sample, and for new compression schemes.

<b>WAVEFORMATEXTENSIBLE</b> can safely be cast to <b>WAVEFORMATEX</b>, because it simply configures the extra bytes specified by <b>WAVEFORMATEX.cbSize</b>.

The <b>dwChannelMask</b> member specifies which channels are present in the multichannel stream. The least significant bit corresponds with the front left speaker, the next least significant bit corresponds to the front right speaker, and so on. The bits, in order of significance, are defined as follows.

<table>
<tr>
<th>Speaker position
            </th>
<th>Flag bit
            </th>
</tr>
<tr>
<td>SPEAKER_FRONT_LEFT</td>
<td>0x1</td>
</tr>
<tr>
<td>SPEAKER_FRONT_RIGHT</td>
<td>0x2</td>
</tr>
<tr>
<td>SPEAKER_FRONT_CENTER</td>
<td>0x4</td>
</tr>
<tr>
<td>SPEAKER_LOW_FREQUENCY</td>
<td>0x8</td>
</tr>
<tr>
<td>SPEAKER_BACK_LEFT</td>
<td>0x10</td>
</tr>
<tr>
<td>SPEAKER_BACK_RIGHT</td>
<td>0x20</td>
</tr>
<tr>
<td>SPEAKER_FRONT_LEFT_OF_CENTER</td>
<td>0x40</td>
</tr>
<tr>
<td>SPEAKER_FRONT_RIGHT_OF_CENTER</td>
<td>0x80</td>
</tr>
<tr>
<td>SPEAKER_BACK_CENTER</td>
<td>0x100</td>
</tr>
<tr>
<td>SPEAKER_SIDE_LEFT</td>
<td>0x200</td>
</tr>
<tr>
<td>SPEAKER_SIDE_RIGHT</td>
<td>0x400</td>
</tr>
<tr>
<td>SPEAKER_TOP_CENTER</td>
<td>0x800</td>
</tr>
<tr>
<td>SPEAKER_TOP_FRONT_LEFT</td>
<td>0x1000</td>
</tr>
<tr>
<td>SPEAKER_TOP_FRONT_CENTER</td>
<td>0x2000</td>
</tr>
<tr>
<td>SPEAKER_TOP_FRONT_RIGHT</td>
<td>0x4000</td>
</tr>
<tr>
<td>SPEAKER_TOP_BACK_LEFT</td>
<td>0x8000</td>
</tr>
<tr>
<td>SPEAKER_TOP_BACK_CENTER</td>
<td>0x10000</td>
</tr>
<tr>
<td>SPEAKER_TOP_BACK_RIGHT</td>
<td>0x20000</td>
</tr>
</table>
 

The channels specified in <b>dwChannelMask</b> must be present in the prescribed order (from least significant bit up). For example, if only SPEAKER_FRONT_LEFT and SPEAKER_FRONT_RIGHT are specified, then the samples for the front left speaker must come first in the interleaved stream. The number of bits set in <b>dwChannelMask</b> should be the same as the number of channels specified in <b>WAVEFORMATEX.nChannels</b>.

For backward compatibility, any wave format that can be specified by a stand-alone <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure can also be defined by a <b>WAVEFORMATEXTENSIBLE</b> structure. Thus, every wave-format tag in mmreg.h has a corresponding <b>SubFormat</b> GUID. The following table shows some typical wave-format tags and their corresponding <b>SubFormat</b> GUIDs. These GUIDs are defined in Ksmedia.h.

<table>
<tr>
<th>Wave-Format Tag
            </th>
<th>SubFormat GUID
            </th>
</tr>
<tr>
<td>WAVE_FORMAT_PCM</td>
<td>KSDATAFORMAT_SUBTYPE_PCM</td>
</tr>
<tr>
<td>WAVE_FORMAT_IEEE_FLOAT</td>
<td>KSDATAFORMAT_SUBTYPE_IEEE_FLOAT</td>
</tr>
<tr>
<td>WAVE_FORMAT_DRM</td>
<td>KSDATAFORMAT_SUBTYPE_DRM</td>
</tr>
<tr>
<td>WAVE_FORMAT_ALAW</td>
<td>KSDATAFORMAT_SUBTYPE_ALAW</td>
</tr>
<tr>
<td>WAVE_FORMAT_MULAW</td>
<td>KSDATAFORMAT_SUBTYPE_MULAW</td>
</tr>
<tr>
<td>WAVE_FORMAT_ADPCM</td>
<td>KSDATAFORMAT_SUBTYPE_ADPCM</td>
</tr>
</table>
 

Because <b>WAVEFORMATEXTENSIBLE</b> is an extended version of <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>, it can describe additional formats that cannot be described by <b>WAVEFORMATEX</b> alone. Vendors are free to define their own <b>SubFormat</b> GUIDs to identify proprietary formats for which no wave-format tags exist.

The following structures, for particular extended formats, are defined as <b>WAVEFORMATEXTENSIBLE</b>.

<table>
<tr>
<th>Definition
            </th>
<th>Value of SubFormat
            </th>
</tr>
<tr>
<td><b>WAVEFORMATIEEEFLOATEX</b></td>
<td>KSDATAFORMAT_SUBTYPE_IEEE_FLOAT</td>
</tr>
<tr>
<td><b>WAVEFORMATPCMEX</b></td>
<td>KSDATAFORMAT_SUBTYPE_PCM</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>

