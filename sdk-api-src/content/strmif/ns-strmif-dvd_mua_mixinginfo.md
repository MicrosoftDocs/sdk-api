---
UID: NS:strmif.tagDVD_MUA_MixingInfo
title: DVD_MUA_MixingInfo (strmif.h)
description: The DVD_MUA_MixingInfo structure describes the surround sound mixing information for the channels in one audio stream in a specified title.
helpviewer_keywords: ["DVD_MUA_MixingInfo","DVD_MUA_MixingInfo structure [DirectShow]","DVD_MUA_MixingInfoStructure","dshow.dvd_mua_mixinginfo","strmif/DVD_MUA_MixingInfo"]
old-location: dshow\dvd_mua_mixinginfo.htm
tech.root: dshow
ms.assetid: df830598-f484-483d-a0dc-e6bd9debbe53
ms.date: 4/26/2023
ms.keywords: DVD_MUA_MixingInfo, DVD_MUA_MixingInfo structure [DirectShow], DVD_MUA_MixingInfoStructure, dshow.dvd_mua_mixinginfo, strmif/DVD_MUA_MixingInfo
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_MUA_MixingInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_MUA_MixingInfo
 - strmif/tagDVD_MUA_MixingInfo
 - DVD_MUA_MixingInfo
 - strmif/DVD_MUA_MixingInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_MUA_MixingInfo
---

# DVD_MUA_MixingInfo structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DVD_MUA_MixingInfo</code> structure describes the surround sound mixing information for the channels in one audio stream in a specified title.

## -struct-fields

### -field fMixTo0

Variable of type BOOL; <b>TRUE</b> means the channel is mixed to channel 0.

### -field fMixTo1

Variable of type BOOL; <b>TRUE</b> means the channel is mixed to channel 1.

### -field fMix0InPhase

Variable of type BOOL; <b>TRUE</b> means the channel is mixed in phase to channel 0.

### -field fMix1InPhase

Variable of type BOOL; <b>TRUE</b> means the channel is mixed in phase to channel 1.

### -field dwSpeakerPosition

The speaker for which this channel is intended. See Remarks.

## -remarks

Applications cannot use the information contained in this structure to change the mixing unless they have a way to communicate with a custom audio decoder that has been inserted manually into the filter graph. The default audio decoder handles Linear Pulse Code Modulated (LPCM) audio using the mixing information on the digital video disc (DVD), but applications have no way to instruct the decoder to modify the mixing values. This means that current DVD playback applications should have no need to access the multichannel-related data structures.

The [DVD_MultichannelAudioAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_multichannelaudioattributes) structure contains information about one audio stream in a specified title. An array of up to eight <code>DVD_MUA_MixingInfo</code> structures will be populated in this structure, if the following conditions are true.

<ul>
<li>DVD_AudioAttributes.AppMode = DVD_AudioMode_Surround</li>
<li>DVD_AudioAttributes.AudioFormat = DVD_AudioFormat_LPCM</li>
<li>DVD_AudioAttributes.fHasMultichannelInfo = 1</li>
</ul>
Possible values for <b>dwSpeakerPosition</b> are defined in Ksmedia.h as follows:

<table>
<tr>
<th>Define
            </th>
<th>Value
            </th>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_LEFT</td>
<td>0x1</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_RIGHT</td>
<td>0x2</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_CENTER</td>
<td>0x4</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SURROUND_LEFT</td>
<td>0x8</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SURROUND_RIGHT</td>
<td>0x10</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SUBWOOFER</td>
<td>0x20</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_LEFT_OF_CENTER</td>
<td>0x40</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_RIGHT_OF_CENTER</td>
<td>0x80</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SURROUND_MONO</td>
<td>0x100</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SIDE_LEFT</td>
<td>0x200</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_SIDE_RIGHT</td>
<td>0x400</td>
</tr>
<tr>
<td>KSAUDIO_SPEAKER_TOP</td>
<td>0x800</td>
</tr>
</table>

## -see-also

[DVD_AudioAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes)



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>