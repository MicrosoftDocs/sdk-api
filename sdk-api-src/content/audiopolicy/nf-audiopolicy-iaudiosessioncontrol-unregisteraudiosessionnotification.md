---
UID: NF:audiopolicy.IAudioSessionControl.UnregisterAudioSessionNotification
title: IAudioSessionControl::UnregisterAudioSessionNotification (audiopolicy.h)
description: The UnregisterAudioSessionNotification method deletes a previous registration by the client to receive notifications.
helpviewer_keywords: ["IAudioSessionControl interface [Core Audio]","UnregisterAudioSessionNotification method","IAudioSessionControl.UnregisterAudioSessionNotification","IAudioSessionControl::UnregisterAudioSessionNotification","IAudioSessionControlUnregisterAudioSessionNotification","UnregisterAudioSessionNotification","UnregisterAudioSessionNotification method [Core Audio]","UnregisterAudioSessionNotification method [Core Audio]","IAudioSessionControl interface","audiopolicy/IAudioSessionControl::UnregisterAudioSessionNotification","coreaudio.iaudiosessioncontrol_unregisteraudiosessionnotification"]
old-location: coreaudio\iaudiosessioncontrol_unregisteraudiosessionnotification.htm
tech.root: CoreAudio
ms.assetid: 1b496d58-c855-44b8-b437-6cb6017dcc9d
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl interface [Core Audio],UnregisterAudioSessionNotification method, IAudioSessionControl.UnregisterAudioSessionNotification, IAudioSessionControl::UnregisterAudioSessionNotification, IAudioSessionControlUnregisterAudioSessionNotification, UnregisterAudioSessionNotification, UnregisterAudioSessionNotification method [Core Audio], UnregisterAudioSessionNotification method [Core Audio],IAudioSessionControl interface, audiopolicy/IAudioSessionControl::UnregisterAudioSessionNotification, coreaudio.iaudiosessioncontrol_unregisteraudiosessionnotification
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
 - IAudioSessionControl::UnregisterAudioSessionNotification
 - audiopolicy/IAudioSessionControl::UnregisterAudioSessionNotification
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
 - IAudioSessionControl.UnregisterAudioSessionNotification
---

# IAudioSessionControl::UnregisterAudioSessionNotification


## -description

The <b>UnregisterAudioSessionNotification</b> method deletes a previous registration by the client to receive notifications.

## -parameters

### -param NewNotifications [in]

Pointer to a client-implemented <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface. The client passed this same interface pointer to the session manager in a previous call to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a> method. If the <b>UnregisterAudioSessionNotification</b> method succeeds, it calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the client's <b>IAudioSessionEvents</b> interface.

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
Parameter <i>NewNotifications</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface was not previously registered by the client or has already been removed.

</td>
</tr>
</table>

## -remarks

The client calls this method when it no longer needs to receive notifications. The <b>UnregisterAudioSessionNotification</b> method removes the registration of an <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface that the client previously registered with the session manager by calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

Before the client releases its final reference to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface, it should call <b>UnregisterAudioSessionNotification</b> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioSessionEvents</b> and <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> objects. Note that <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">RegisterAudioSessionNotification</a> calls the client's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IAudioSessionEvents::AddRef</a> method, and <b>UnregisterAudioSessionNotification</b> calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IAudioSessionEvents::Release</a> method. If the client errs by releasing its reference to the <b>IAudioSessionEvents</b> interface before calling <b>UnregisterAudioSessionNotification</b>, the session manager never releases its reference to the <b>IAudioSessionEvents</b> interface. For example, a poorly designed <b>IAudioSessionEvents</b> implementation might call <b>UnregisterAudioSessionNotification</b> from the destructor for the <b>IAudioSessionEvents</b> object. In this case, the client will not call <b>UnregisterAudioSessionNotification</b> until the session manager releases its reference to the <b>IAudioSessionEvents</b> interface, and the session manager will not release its reference to the <b>IAudioSessionEvents</b> interface until the client calls <b>UnregisterAudioSessionNotification</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface in the Windows SDK documentation.

For a code example that calls the <b>UnregisterAudioSessionNotification</b> method, see <a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>