---
UID: NF:audioclient.IChannelAudioVolume.GetChannelVolume
title: IChannelAudioVolume::GetChannelVolume (audioclient.h)
description: The GetChannelVolume method retrieves the volume level for the specified channel in the audio session.helpviewer_keywords: ["GetChannelVolume","GetChannelVolume method [Core Audio]","GetChannelVolume method [Core Audio]","IChannelAudioVolume interface","IChannelAudioVolume interface [Core Audio]","GetChannelVolume method","IChannelAudioVolume.GetChannelVolume","IChannelAudioVolume::GetChannelVolume","IChannelAudioVolumeGetChannelVolume","audioclient/IChannelAudioVolume::GetChannelVolume","coreaudio.ichannelaudiovolume_getchannelvolume"]
old-location: coreaudio\ichannelaudiovolume_getchannelvolume.htm
tech.root: CoreAudio
ms.assetid: adc871ff-fb77-4d72-b33b-a2773bed2569
ms.date: 12/05/2018
ms.keywords: GetChannelVolume, GetChannelVolume method [Core Audio], GetChannelVolume method [Core Audio],IChannelAudioVolume interface, IChannelAudioVolume interface [Core Audio],GetChannelVolume method, IChannelAudioVolume.GetChannelVolume, IChannelAudioVolume::GetChannelVolume, IChannelAudioVolumeGetChannelVolume, audioclient/IChannelAudioVolume::GetChannelVolume, coreaudio.ichannelaudiovolume_getchannelvolume
f1_keywords:
- audioclient/IChannelAudioVolume.GetChannelVolume
dev_langs:
- c++
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Audioclient.h
api_name:
- IChannelAudioVolume.GetChannelVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IChannelAudioVolume::GetChannelVolume


## -description



The <b>GetChannelVolume</b> method retrieves the volume level for the specified channel in the audio session.




## -parameters




### -param dwIndex [in]

The channel number. If the stream format for the audio session has <i>N</i> channels, then the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels, call the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a> method.


### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the volume level of the specified channel. The volume level is in the range 0.0 to 1.0.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>dwIndex</i> is set to an invalid channel number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfLevel</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



Clients can call the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setallvolumes">IChannelAudioVolume::SetAllVolumes</a> or <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setchannelvolume">IChannelAudioVolume::SetChannelVolume</a> method to set the per-channel volume levels in an audio session.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setallvolumes">IChannelAudioVolume::SetAllVolumes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setchannelvolume">IChannelAudioVolume::SetChannelVolume</a>
 

 

