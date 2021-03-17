---
UID: NF:audiopolicy.IAudioSessionControl2.SetDuckingPreference
title: IAudioSessionControl2::SetDuckingPreference (audiopolicy.h)
description: The SetDuckingPreference method enables or disables the default stream attenuation experience (auto-ducking) provided by the system.
helpviewer_keywords: ["IAudioSessionControl2 interface [Core Audio]","SetDuckingPreference method","IAudioSessionControl2.SetDuckingPreference","IAudioSessionControl2::SetDuckingPreference","SetDuckingPreference","SetDuckingPreference method [Core Audio]","SetDuckingPreference method [Core Audio]","IAudioSessionControl2 interface","audiopolicy/IAudioSessionControl2::SetDuckingPreference","coreaudio.iaudiosessioncontrol2_setduckingpreference"]
old-location: coreaudio\iaudiosessioncontrol2_setduckingpreference.htm
tech.root: CoreAudio
ms.assetid: 6689d7e4-9c45-483d-9f46-14d157726b02
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl2 interface [Core Audio],SetDuckingPreference method, IAudioSessionControl2.SetDuckingPreference, IAudioSessionControl2::SetDuckingPreference, SetDuckingPreference, SetDuckingPreference method [Core Audio], SetDuckingPreference method [Core Audio],IAudioSessionControl2 interface, audiopolicy/IAudioSessionControl2::SetDuckingPreference, coreaudio.iaudiosessioncontrol2_setduckingpreference
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioSessionControl2::SetDuckingPreference
 - audiopolicy/IAudioSessionControl2::SetDuckingPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionControl2.SetDuckingPreference
---

# IAudioSessionControl2::SetDuckingPreference


## -description

The <b>SetDuckingPreference</b> method enables or disables the default stream attenuation experience (auto-ducking) provided by the system.

## -parameters

### -param optOut [in]

A <b>BOOL</b> variable that enables or disables system auto-ducking.

## -returns

If the method succeeds, it returns S_OK.
          If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>AUDCLNT_E_DEVICE_INVALIDATED</dt>
</dl>
</td>
<td width="60%">
The audio session is disconnected on the default audio device.

</td>
</tr>
</table>

## -remarks

    By default, the system adjusts the volume for all currently playing sounds when the system starts a communication session and receives a new communication stream on the default communication device. For more information about this feature, see <a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>.

If the application passes <b>TRUE</b> in <i>optOut</i>, the system disables the <a href="/windows/desktop/CoreAudio/stream-attenuation">Default Ducking Experience</a>. For more information, see <a href="/windows/desktop/CoreAudio/disabling-the-ducking-experience">Disabling the Default Ducking Experience</a>.

To provide a custom implementation, the application needs to get notifications from the system when it opens or closes the communication stream. To receive the notifications, the application must call this method before registering itself by calling <b>IAudioSessionManager2::RegisterForDuckNotification</b>. For more information and example code, see <a href="/windows/desktop/CoreAudio/getting-ducking-events-from-a-communication-device">Getting Ducking Events</a>.

If the application passes <b>FALSE</b> in <i>optOut</i>, the application provides the default stream attenuation experience provided by the system.

We recommend that the application call <b>SetDuckingPreference</b> during stream creation.  However, this method can be called dynamically during the session to change the initial preference.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2">IAudioSessionControl2</a>