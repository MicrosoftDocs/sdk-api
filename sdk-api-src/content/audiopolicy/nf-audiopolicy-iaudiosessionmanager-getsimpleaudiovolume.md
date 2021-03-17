---
UID: NF:audiopolicy.IAudioSessionManager.GetSimpleAudioVolume
title: IAudioSessionManager::GetSimpleAudioVolume (audiopolicy.h)
description: The GetSimpleAudioVolume method retrieves a simple audio volume control.
helpviewer_keywords: ["GetSimpleAudioVolume","GetSimpleAudioVolume method [Core Audio]","GetSimpleAudioVolume method [Core Audio]","IAudioSessionManager interface","IAudioSessionManager interface [Core Audio]","GetSimpleAudioVolume method","IAudioSessionManager.GetSimpleAudioVolume","IAudioSessionManager::GetSimpleAudioVolume","IAudioSessionManagerGetSimpleAudioVolume","audiopolicy/IAudioSessionManager::GetSimpleAudioVolume","coreaudio.iaudiosessionmanager_getsimpleaudiovolume"]
old-location: coreaudio\iaudiosessionmanager_getsimpleaudiovolume.htm
tech.root: CoreAudio
ms.assetid: 2f3c5a40-308f-48b4-b35c-aebd0cc6b849
ms.date: 12/05/2018
ms.keywords: GetSimpleAudioVolume, GetSimpleAudioVolume method [Core Audio], GetSimpleAudioVolume method [Core Audio],IAudioSessionManager interface, IAudioSessionManager interface [Core Audio],GetSimpleAudioVolume method, IAudioSessionManager.GetSimpleAudioVolume, IAudioSessionManager::GetSimpleAudioVolume, IAudioSessionManagerGetSimpleAudioVolume, audiopolicy/IAudioSessionManager::GetSimpleAudioVolume, coreaudio.iaudiosessionmanager_getsimpleaudiovolume
req.header: audiopolicy.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSessionManager::GetSimpleAudioVolume
 - audiopolicy/IAudioSessionManager::GetSimpleAudioVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionManager.GetSimpleAudioVolume
---

# IAudioSessionManager::GetSimpleAudioVolume


## -description

The <b>GetSimpleAudioVolume</b> method retrieves a simple audio volume control.

## -parameters

### -param AudioSessionGuid [in]

Pointer to a session GUID. If the GUID does not identify a session that has been previously opened, the call opens a new but empty session. The Sndvol program does not display a volume-level control for a session unless it contains one or more active streams. If this parameter is <b>NULL</b> or points to the value GUID_NULL, the method assigns the stream to the default session.

### -param StreamFlags [in]

Specifies whether the request is for a cross-process session. Set to <b>TRUE</b> if the session is cross-process. Set to <b>FALSE</b> if the session is not cross-process.

### -param AudioVolume [out]

Pointer to a pointer variable into which the method writes a pointer to the <a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a> interface of the audio volume control object. This interface represents the simple audio volume control for the current process. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>Activate</b> call fails, <i>*AudioVolume</i> is <b>NULL</b>.

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
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>AudioVolume</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager">IAudioSessionManager Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>