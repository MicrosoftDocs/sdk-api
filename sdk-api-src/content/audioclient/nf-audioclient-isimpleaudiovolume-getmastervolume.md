---
UID: NF:audioclient.ISimpleAudioVolume.GetMasterVolume
title: ISimpleAudioVolume::GetMasterVolume (audioclient.h)
description: The GetMasterVolume method retrieves the client volume level for the audio session.
helpviewer_keywords: ["GetMasterVolume","GetMasterVolume method [Core Audio]","GetMasterVolume method [Core Audio]","ISimpleAudioVolume interface","ISimpleAudioVolume interface [Core Audio]","GetMasterVolume method","ISimpleAudioVolume.GetMasterVolume","ISimpleAudioVolume::GetMasterVolume","ISimpleAudioVolumeGetMasterVolume","audioclient/ISimpleAudioVolume::GetMasterVolume","coreaudio.isimpleaudiovolume_getmastervolume"]
old-location: coreaudio\isimpleaudiovolume_getmastervolume.htm
tech.root: CoreAudio
ms.assetid: 362d8e12-a92c-4e0f-b88f-a3937c75d01a
ms.date: 12/05/2018
ms.keywords: GetMasterVolume, GetMasterVolume method [Core Audio], GetMasterVolume method [Core Audio],ISimpleAudioVolume interface, ISimpleAudioVolume interface [Core Audio],GetMasterVolume method, ISimpleAudioVolume.GetMasterVolume, ISimpleAudioVolume::GetMasterVolume, ISimpleAudioVolumeGetMasterVolume, audioclient/ISimpleAudioVolume::GetMasterVolume, coreaudio.isimpleaudiovolume_getmastervolume
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
 - ISimpleAudioVolume::GetMasterVolume
 - audioclient/ISimpleAudioVolume::GetMasterVolume
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
 - ISimpleAudioVolume.GetMasterVolume
---

# ISimpleAudioVolume::GetMasterVolume


## -description

The <b>GetMasterVolume</b> method retrieves the client volume level for the audio session.

## -parameters

### -param pfLevel [out]

Pointer to a <b>float</b> variable into which the method writes the client volume level. The volume level is a value in the range 0.0 to 1.0.

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

This method retrieves the client volume level for the session. This is the volume level that the client set in a previous call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a> method.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a>