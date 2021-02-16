---
UID: NF:audiopolicy.IAudioSessionManager.GetAudioSessionControl
title: IAudioSessionManager::GetAudioSessionControl (audiopolicy.h)
description: The GetAudioSessionControl method retrieves an audio session control.
helpviewer_keywords: ["GetAudioSessionControl","GetAudioSessionControl method [Core Audio]","GetAudioSessionControl method [Core Audio]","IAudioSessionManager interface","IAudioSessionManager interface [Core Audio]","GetAudioSessionControl method","IAudioSessionManager.GetAudioSessionControl","IAudioSessionManager::GetAudioSessionControl","IAudioSessionManagerGetAudioSessionControl","audiopolicy/IAudioSessionManager::GetAudioSessionControl","coreaudio.iaudiosessionmanager_getaudiosessioncontrol"]
old-location: coreaudio\iaudiosessionmanager_getaudiosessioncontrol.htm
tech.root: CoreAudio
ms.assetid: 42de66dd-46df-40af-9d8a-39ee9f91b468
ms.date: 12/05/2018
ms.keywords: GetAudioSessionControl, GetAudioSessionControl method [Core Audio], GetAudioSessionControl method [Core Audio],IAudioSessionManager interface, IAudioSessionManager interface [Core Audio],GetAudioSessionControl method, IAudioSessionManager.GetAudioSessionControl, IAudioSessionManager::GetAudioSessionControl, IAudioSessionManagerGetAudioSessionControl, audiopolicy/IAudioSessionManager::GetAudioSessionControl, coreaudio.iaudiosessionmanager_getaudiosessioncontrol
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
 - IAudioSessionManager::GetAudioSessionControl
 - audiopolicy/IAudioSessionManager::GetAudioSessionControl
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
 - IAudioSessionManager.GetAudioSessionControl
---

# IAudioSessionManager::GetAudioSessionControl


## -description

The <b>GetAudioSessionControl</b> method retrieves an audio session control.

## -parameters

### -param AudioSessionGuid [in]

Pointer to a session GUID. If the GUID does not identify a session that has been previously opened, the call opens a new but empty session. The Sndvol program does not display a volume-level control for a session unless it contains one or more active streams. If this parameter is <b>NULL</b> or points to the value GUID_NULL, the method assigns the stream to the default session.

### -param StreamFlags [in]

Specifies the status of the flags for the audio stream.

### -param SessionControl [out]

Pointer to a pointer variable into which the method writes a pointer to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> interface of the audio session control object. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the call fails, <i>*SessionControl</i> is <b>NULL</b>.

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
Parameter <i>SessionControl</i> is <b>NULL</b>.

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

## -remarks

For a code example that calls this method, see <a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager">IAudioSessionManager Interface</a>