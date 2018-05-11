---
UID: NS:strmif.tagDVD_MUA_MixingInfo
title: tagDVD_MUA_MixingInfo
author: windows-driver-content
description: The DVD_MUA_MixingInfo structure describes the surround sound mixing information for the channels in one audio stream in a specified title.
old-location: dshow\dvd_mua_mixinginfo.htm
old-project: DirectShow
ms.assetid: df830598-f484-483d-a0dc-e6bd9debbe53
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DVD_MUA_MixingInfo, DVD_MUA_MixingInfo structure [DirectShow], DVD_MUA_MixingInfoStructure, dshow.dvd_mua_mixinginfo, strmif/DVD_MUA_MixingInfo, tagDVD_MUA_MixingInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DVD_MUA_MixingInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_MUA_MixingInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_MUA_MixingInfo structure


## -description



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

The <a href="https://msdn.microsoft.com/8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d">DVD_MultichannelAudioAttributes</a> structure contains information about one audio stream in a specified title. An array of up to eight <code>DVD_MUA_MixingInfo</code> structures will be populated in this structure, if the following conditions are true.

<ul>
<li>DVD_AudioAttributes.AppMode = DVD_AudioMode_Surround</li>
<li>DVD_AudioAttributes.AudioFormat = DVD_AudioFormat_LPCM</li>
<li>DVD_AudioAttributes.fHasMultichannelInfo = 1</li>
</ul>
Possible values for <b>dwSpeakerPosition</b> are defined in Ksmedia.h as follows:

<table>
<tr>
<th>
              Define
            </th>
<th>
              Value
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




<a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

