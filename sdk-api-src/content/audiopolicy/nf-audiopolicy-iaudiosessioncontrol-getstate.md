---
UID: NF:audiopolicy.IAudioSessionControl.GetState
title: IAudioSessionControl::GetState (audiopolicy.h)
description: The GetState method retrieves the current state of the audio session.
helpviewer_keywords: ["GetState","GetState method [Core Audio]","GetState method [Core Audio]","IAudioSessionControl interface","IAudioSessionControl interface [Core Audio]","GetState method","IAudioSessionControl.GetState","IAudioSessionControl::GetState","IAudioSessionControlGetState","audiopolicy/IAudioSessionControl::GetState","coreaudio.iaudiosessioncontrol_getstate"]
old-location: coreaudio\iaudiosessioncontrol_getstate.htm
tech.root: CoreAudio
ms.assetid: 9c0188a1-7982-40f0-9040-bda00473160c
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Core Audio], GetState method [Core Audio],IAudioSessionControl interface, IAudioSessionControl interface [Core Audio],GetState method, IAudioSessionControl.GetState, IAudioSessionControl::GetState, IAudioSessionControlGetState, audiopolicy/IAudioSessionControl::GetState, coreaudio.iaudiosessioncontrol_getstate
req.header: audiopolicy.h
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
 - IAudioSessionControl::GetState
 - audiopolicy/IAudioSessionControl::GetState
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
 - IAudioSessionControl.GetState
---

# IAudioSessionControl::GetState


## -description

The <b>GetState</b> method retrieves the current state of the audio session.

## -parameters

### -param pRetVal [out]

Pointer to a variable into which the method writes the current session state. The state must be one of the following <a href="/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audiosessionstate">AudioSessionState</a> enumeration values:

AudioSessionStateActive

AudioSessionStateInactive

AudioSessionStateExpired

These values indicate that the session state is active, inactive, or expired, respectively. For more information, see Remarks.

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
Parameter <i>pRetVal</i> is <b>NULL</b>.

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

This method indicates whether the state of the session is active, inactive, or expired. The state is active if the session has one or more streams that are running. The state changes from active to inactive when the last running stream in the session stops. The session state changes to expired when the client destroys the last stream in the session by releasing all references to the stream object.

The Sndvol program displays volume and mute controls for sessions that are in the active and inactive states. When a session expires, Sndvol stops displaying the controls for that session. If a session has previously expired, but the session state changes to active (because a stream in the session begins running) or inactive (because a client assigns a new stream to the session), Sndvol resumes displaying the controls for the session.

The client creates a stream by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method. At the time that it creates a stream, the client assigns the stream to a session. A session begins when a client assigns the first stream to the session. Initially, the session is in the inactive state. The session state changes to active when the first stream in the session begins running. The session terminates when a client releases the final reference to the last remaining stream object in the session.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>