---
UID: NS:mmreg.tWAVEFORMATEX
title: WAVEFORMATEX (mmreg.h)
description: The WAVEFORMATEX structure specifies the data format of a wave audio stream.
helpviewer_keywords: ["*LPWAVEFORMATEX","*NPWAVEFORMATEX","*PWAVEFORMATEX","WAVEFORMATEX","WAVEFORMATEX structure [Audio Devices]","aud-prop_f0d9c096-fa87-43d5-812b-de4d08358342.xml","audio.waveformatex","mmreg/WAVEFORMATEX"]
old-location: audio\waveformatex.htm
tech.root: audio
ms.assetid: f2f050d6-afe2-4647-932b-1287f4538702
ms.date: 12/05/2018
ms.keywords: '*LPWAVEFORMATEX, *NPWAVEFORMATEX, *PWAVEFORMATEX, WAVEFORMATEX, WAVEFORMATEX structure [Audio Devices], aud-prop_f0d9c096-fa87-43d5-812b-de4d08358342.xml, audio.waveformatex, mmreg/WAVEFORMATEX'
req.header: mmreg.h
req.include-header: Mmsystem.h, Mmreg.h, Mmsystem.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WAVEFORMATEX, *PWAVEFORMATEX, *NPWAVEFORMATEX, *LPWAVEFORMATEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tWAVEFORMATEX
 - mmreg/tWAVEFORMATEX
 - PWAVEFORMATEX
 - mmreg/PWAVEFORMATEX
 - WAVEFORMATEX
 - mmreg/WAVEFORMATEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmreg.h
api_name:
 - WAVEFORMATEX
---

# WAVEFORMATEX structure


## -description

The WAVEFORMATEX structure specifies the data format of a wave audio stream.

## -struct-fields

### -field wFormatTag

Specifies the waveform audio format type. For more information, see the following Remarks section.

### -field nChannels

Specifies the number of channels of audio data. For monophonic audio, set this member to 1. For stereo, set this member to 2.

### -field nSamplesPerSec

Specifies the sample frequency at which each channel should be played or recorded. If <b>wFormatTag</b> = WAVE_FORMAT_PCM, then common values for <b>nSamplesPerSec</b> are 8.0 kHz, 11.025 kHz, 22.05 kHz, and 44.1 kHz. For example, to specify a sample frequency of 11.025 kHz, set <b>nSamplesPerSec</b> to 11025. For non-PCM formats, this member should be computed according to the manufacturer's specification of the format tag.

### -field nAvgBytesPerSec

Specifies the required average data transfer rate in bytes per second. This value is useful for estimating buffer size.

### -field nBlockAlign

Specifies the block alignment in bytes. The block alignment is the size of the minimum atomic unit of data for the <b>wFormatTag</b> format type. If <b>wFormatTag</b> = WAVE_FORMAT_PCM or <b>wFormatTag</b> = WAVE_FORMAT_IEEE_FLOAT, set <b>nBlockAlign</b> to <code>(nChannels*wBitsPerSample)/8</code>, which is the size of a single audio frame. For non-PCM formats, this member should be computed according to the manufacturer's specification for the format tag.

Playback and record software should process a multiple of <b>nBlockAlign</b> bytes of data at a time. Data written to and read from a device should always start at the beginning of a block.

### -field wBitsPerSample

Specifies the number of bits per sample for the format type specified by <b>wFormatTag</b>. If <b>wFormatTag</b> = WAVE_FORMAT_PCM, then <b>wBitsPerSample</b> should be set to either 8 or 16. If <b>wFormatTag</b> = WAVE_FORMAT_IEEE_FLOAT, <b>wBitsPerSample</b> should be set to 32. For non-PCM formats, set the value of this member according to the manufacturer's specification for the format tag. Some compression schemes cannot define a value for <b>wBitsPerSample</b>. In this case, set <b>wBitsPerSample</b> to zero.

### -field cbSize

Specifies the size, in bytes, of extra format information appended to the end of the WAVEFORMATEX structure. This information can be used by non-PCM formats to store extra attributes for the <b>wFormatTag</b>. If no extra information is required by the <b>wFormatTag</b>, set this member to zero. For WAVE_FORMAT_PCM formats, clients should ignore this member (its value is implicitly zero). Because all clients might not follow this rule, we recommend that you initialize <b>cbSize</b> to zero for WAVE_FORMAT_PCM formats.

## -remarks

The WAVEFORMATEX structure can describe only a subset of the formats that can be described by the <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a> structure. For example, WAVEFORMATEX can describe mono or (two-channel) stereo pulse-code modulated (PCM) streams with 8-bit or 16-bit integer sample values, or with 32-bit floating-point sample values. In addition, WAVEFORMATEX can describe popular non-PCM formats such as AC-3 and WMA Pro.

WAVEFORMATEX can unambiguously describe mono or stereo PCM formats for which the number of valid bits per sample is the same as the sample container size. To describe a PCM format with more than two channels requires WAVEFORMATEXTENSIBLE, which has a channel mask to specify the speaker configuration (that is, the mapping of channels to physical speaker positions). To describe a PCM format for which the number of valid bits per sample is less than the sample container size (for example, a 20-bit sample stored in a three-byte container) requires WAVEFORMATEXTENSIBLE, which specifies both the number of valid sample bits and the sample container size.

WAVEFORMATEX can describe non-PCM formats for which 16-bit format tags are defined in header file Mmreg.h (for example, WAVE_FORMAT_MPEG). The <b>wFormatTag</b> member of WAVEFORMATEX contains the format tag. Specify a non-PCM format for which a format tag is not defined in Mmreg.h  by a WAVEFORMATEXTENSIBLE structure, which contains a GUID that identifies the format. If necessary, a hardware vendor can independently generate a GUID value to identify a new format. Registering the GUID with Microsoft is unnecessary.

For more information about the differences between WAVEFORMATEX and WAVEFORMATEXTENSIBLE, see <a href="/windows-hardware/drivers/audio/extensible-wave-format-descriptors">Extensible Wave-Format Descriptors</a>.

The <b>wFormatTag</b> member is set to one of the wave format tags that are defined in Mmreg.h. Tags for some of the more common nonproprietary formats are listed in the following table.

<table>
<tr>
<th>wFormatTag Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WAVE_FORMAT_PCM

</td>
<td>
PCM (pulse-code modulated) data in integer format.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_IEEE_FLOAT

</td>
<td>
PCM data in IEEE floating-point format.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_DRM

</td>
<td>
DRM-encoded format (for digital-audio content protected by Microsoft <a href="/windows-hardware/drivers/audio/digital-rights-management">Digital Rights Management</a>).

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_EXTENSIBLE

</td>
<td>
Extensible WAVEFORMATEX structure (see <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>).

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_ALAW

</td>
<td>
A-law-encoded format.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_MULAW

</td>
<td>
Mu-law-encoded format.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_ADPCM

</td>
<td>
ADPCM (adaptive differential pulse-code modulated) data.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_MPEG

</td>
<td>
MPEG-1 data format (stream conforms to ISO 11172-3 Audio specification).

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_DOLBY_AC3_SPDIF

</td>
<td>
AC-3 (aka Dolby Digital) over S/PDIF.

</td>
</tr>
<tr>
<td>
WAVE_FORMAT_WMASPDIF

</td>
<td>
Windows Media Audio (WMA) Pro over S/PDIF.

</td>
</tr>
</table>
 

See Mmreg.h for the complete list of WAVE_FORMAT_<i>Xxx</i> formats.

WAVEFORMATEX is nearly identical to the PCMWAVEFORMAT structure, which is an obsolete structure used to specify PCM formats. The only difference is that WAVEFORMATEX contains a <b>cbSize</b> member and PCMWAVEFORMAT does not. By convention, <b>cbSize</b> should be ignored when <b>wFormatTag</b> = WAVE_FORMAT_PCM (because <b>cbSize</b> is implicitly zero). This convention allows driver software to treat the WAVEFORMATEX and PCMWAVEFORMAT structures identically in the case of a PCM format. For more information about PCMWAVEFORMAT, see the Microsoft Windows SDK documentation.

If <b>wFormatTag</b> = WAVE_FORMAT_PCM or <b>wFormatTag</b> = WAVE_FORMAT_IEEE_FLOAT, set <b>cbSize</b> to zero. For all other values of <b>wFormatTag</b>, <b>cbSize</b> specifies how many bytes of additional format data are appended to the WAVEFORMATEX structure.

If <b>wFormatTag</b> = WAVE_FORMAT_EXTENSIBLE, set <b>cbSize</b> to <code>sizeof(WAVEFORMATEXTENSIBLE)-sizeof(WAVEFORMATEX)</code> plus the size of any format-specific data that is appended to the WAVEFORMATEXTENSIBLE structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>