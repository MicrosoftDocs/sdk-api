---
UID: NS:mmreg.WAVEFORMATEXTENSIBLE
title: WAVEFORMATEXTENSIBLE
author: windows-driver-content
description: The WAVEFORMATEXTENSIBLE structure defines the format of waveform-audio data for formats having more than two channels or higher sample resolutions than allowed by WAVEFORMATEX.
old-location: dshow\waveformatextensible.htm
old-project: DirectShow
ms.assetid: b16cdcab-fa4f-4c9a-b1f3-af459bd33245
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*LPWAVEFORMATIEEEFLOATEX, *LPWAVEFORMATPCMEX, *NPWAVEFORMATIEEEFLOATEX, *NPWAVEFORMATPCMEX, *PWAVEFORMATEXTENSIBLE, *PWAVEFORMATIEEEFLOATEX, *PWAVEFORMATPCMEX, KSDATAFORMAT_SUBTYPE_ADPCM, KSDATAFORMAT_SUBTYPE_ALAW, KSDATAFORMAT_SUBTYPE_DRM, KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL, KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS, KSDATAFORMAT_SUBTYPE_IEEE_FLOAT, KSDATAFORMAT_SUBTYPE_MPEG, KSDATAFORMAT_SUBTYPE_MULAW, KSDATAFORMAT_SUBTYPE_PCM, PWAVEFORMATEXTENSIBLE, PWAVEFORMATEXTENSIBLE structure pointer [DirectShow], WAVEFORMATEXTENSIBLE, WAVEFORMATEXTENSIBLE structure [DirectShow], WAVEFORMATEXTENSIBLEStructure, WAVEFORMATIEEEFLOATEX, WAVEFORMATPCMEX, dshow.waveformatextensible, ksmedia/PWAVEFORMATEXTENSIBLE, ksmedia/WAVEFORMATEXTENSIBLE, mmreg/PWAVEFORMATEXTENSIBLE, mmreg/WAVEFORMATEXTENSIBLE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mmreg.h
req.include-header: 
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
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MMReg.h
-	Ksmedia.h
api_name:
-	WAVEFORMATEXTENSIBLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# WAVEFORMATEXTENSIBLE structure


## -description



The <b>WAVEFORMATEXTENSIBLE</b> structure defines the format of waveform-audio data for formats having more than two channels or higher sample resolutions than allowed by <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>.




## -struct-fields




### -field Format


<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that specifies the basic format. The <b>wFormatTag</b> member must be WAVE_FORMAT_EXTENSIBLE, defined in Mmreg.h. The <b>cbSize</b> member must be at least 22.


### -field Samples

A union that contains the following members.


### -field Samples.wValidBitsPerSample

Number of bits of precision in the signal. Usually equal to <b>WAVEFORMATEX.wBitsPerSample</b>. However, <b>wBitsPerSample</b> is the container size and must be a multiple of 8, whereas <b>wValidBitsPerSample</b> can be any value not exceeding the container size. For example, if the format uses 20-bit samples, <b>wBitsPerSample</b> must be at least 24, but <b>wValidBitsPerSample</b> is 20.


### -field Samples.wSamplesPerBlock

Number of samples contained in one compressed block of audio data. This value is used in buffer estimation. This value is used with compressed formats that have a fixed number of samples within each block. This value can be set to zero if a variable number of samples is contained in each block of compressed audio data. In this case, buffer estimation and position information needs to be obtained in other ways.


### -field Samples.wReserved


              Reserved. Set to zero.
            


### -field dwChannelMask


            Bitmask specifying the assignment of channels in the stream to speaker positions. See Remarks.
          


### -field SubFormat


            A GUID that specifies the format of the audio data. 
          The following GUIDs are defined in Ksmedia.h.
Third parties can define additional GUIDs.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_ADPCM"></a><a id="ksdataformat_subtype_adpcm"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_ADPCM</b></dt>
</dl>
</td>
<td width="60%">
Adaptive delta pulse code modulation (ADPCM)

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_ALAW"></a><a id="ksdataformat_subtype_alaw"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_ALAW</b></dt>
</dl>
</td>
<td width="60%">
A-law coding.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_DRM"></a><a id="ksdataformat_subtype_drm"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_DRM</b></dt>
</dl>
</td>
<td width="60%">
DRM-encoded format for digital-audio content protected by Microsoft Digital Rights Management.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS"></a><a id="ksdataformat_subtype_iec61937_dolby_digital_plus"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS</b></dt>
</dl>
</td>
<td width="60%">
Dolby Digital Plus formatted for HDMI output.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL"></a><a id="ksdataformat_subtype_iec61937_dolby_digital"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</b></dt>
</dl>
</td>
<td width="60%">
Dolby Digital Plus formatted for S/PDIF or HDMI output.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_IEEE_FLOAT"></a><a id="ksdataformat_subtype_ieee_float"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_IEEE_FLOAT</b></dt>
</dl>
</td>
<td width="60%">
IEEE floating-point audio.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_MPEG"></a><a id="ksdataformat_subtype_mpeg"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_MPEG</b></dt>
</dl>
</td>
<td width="60%">
MPEG-1 audio payload.

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_MULAW"></a><a id="ksdataformat_subtype_mulaw"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_MULAW</b></dt>
</dl>
</td>
<td width="60%">
μ-law coding

</td>
</tr>
<tr>
<td width="40%"><a id="KSDATAFORMAT_SUBTYPE_PCM"></a><a id="ksdataformat_subtype_pcm"></a><dl>
<dt><b>KSDATAFORMAT_SUBTYPE_PCM</b></dt>
</dl>
</td>
<td width="60%">
PCM audio.

</td>
</tr>
</table>
 


## -remarks




          The <b>WAVEFORMATEXTENSIBLE</b> structure can describe any format that can be described by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure, but provides additional support for more than two channels, for greater precision in the number of bits per sample, and for new compression schemes.

The <b>dwChannelMask</b> member specifies which channels are present in the multichannel stream. The least significant bit corresponds with the front left speaker, the next least significant bit corresponds to the front right speaker, and so on. The bits, in order of significance, are defined in Ksmedia.h and Mmreg.h as follows.

<table>
<tr>
<th>
              Speaker position
            </th>
<th>
              Flag bit
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
 

The following constants define some standard speaker configurations as bitwise ORs of the flags shown in the previous table.

<table>
<tr>
<th>
              Value
            </th>
<th>
              Description
            </th>
<th>
              Speakers
            </th>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_MONO</td>
<td>Mono</td>
<td>Front center (C)</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_STEREO</td>
<td>Stereo</td>
<td>Front left (L), front right (R)</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_QUAD</td>
<td>Quadraphonic</td>
<td>L, R, back left (Lb), back right (Rb)</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SURROUND</td>
<td>Surround</td>
<td>L, R, front center (C), back center (Cb)</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_5POINT1</td>
<td>5.1 channel</td>
<td>L, R, C, Lb, Rb, low frequency (LFE)</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_7POINT1</td>
<td>7.1 channel</td>
<td>L, R, C, Lb, Rb, front left-of-center, front right-of-center, LFE</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_5POINT1_SURROUND</td>
<td>5.1 channel surround</td>
<td>L, R, C, side left (Ls), side right (Rs), LFE</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_7POINT1_SURROUND</td>
<td>7.1 channel surround</td>
<td>L, R, C, Lb, Rb, Ls, Rs, LFE</td>
</tr>
</table>
 

For more information on this structure, see the document <a href="https://msdn.microsoft.com/library/windows/hardware/dn653308">Multiple Channel Audio Data and WAVE Files</a>, available at www.microsoft.com.



