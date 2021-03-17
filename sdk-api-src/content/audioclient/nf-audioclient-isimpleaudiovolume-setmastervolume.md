---
UID: NF:audioclient.ISimpleAudioVolume.SetMasterVolume
title: ISimpleAudioVolume::SetMasterVolume (audioclient.h)
description: The SetMasterVolume method sets the master volume level for the audio session.
helpviewer_keywords: ["ISimpleAudioVolume interface [Core Audio]","SetMasterVolume method","ISimpleAudioVolume.SetMasterVolume","ISimpleAudioVolume::SetMasterVolume","ISimpleAudioVolumeSetMasterVolume","SetMasterVolume","SetMasterVolume method [Core Audio]","SetMasterVolume method [Core Audio]","ISimpleAudioVolume interface","audioclient/ISimpleAudioVolume::SetMasterVolume","coreaudio.isimpleaudiovolume_setmastervolume"]
old-location: coreaudio\isimpleaudiovolume_setmastervolume.htm
tech.root: CoreAudio
ms.assetid: 895a8564-5f06-4e20-abcc-d960d4002eb0
ms.date: 12/05/2018
ms.keywords: ISimpleAudioVolume interface [Core Audio],SetMasterVolume method, ISimpleAudioVolume.SetMasterVolume, ISimpleAudioVolume::SetMasterVolume, ISimpleAudioVolumeSetMasterVolume, SetMasterVolume, SetMasterVolume method [Core Audio], SetMasterVolume method [Core Audio],ISimpleAudioVolume interface, audioclient/ISimpleAudioVolume::SetMasterVolume, coreaudio.isimpleaudiovolume_setmastervolume
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimpleAudioVolume::SetMasterVolume
 - audioclient/ISimpleAudioVolume::SetMasterVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - ISimpleAudioVolume.SetMasterVolume
---

# ISimpleAudioVolume::SetMasterVolume


## -description

The <b>SetMasterVolume</b> method sets the master volume level for the audio session.

## -parameters

### -param fLevel [in]

The new master volume level. Valid volume levels are in the range 0.0 to 1.0.

### -param EventContext [in]

Pointer to the event-context GUID. If a call to this method generates a volume-change event, the session manager sends notifications to all clients that have registered <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interfaces with the session manager. The session manager includes the <i>EventContext</i> pointer value with each notification. Upon receiving a notification, a client can determine whether it or another client is the source of the event by inspecting the <i>EventContext</i> value. This scheme depends on the client selecting a value for this parameter that is unique among all clients in the session. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
Parameter <i>fLevel</i> is not in the range 0.0 to 1.0.

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

This method generates a volume-change event only if the method call changes the volume level of the session. For example, if the volume level is 0.4 when the call occurs, and the call sets the volume level to 0.4, no event is generated.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-getmastervolume">ISimpleAudioVolume::GetMasterVolume</a>