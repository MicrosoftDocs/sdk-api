---
UID: NF:audiopolicy.IAudioSessionControl.SetDisplayName
title: IAudioSessionControl::SetDisplayName (audiopolicy.h)
description: The SetDisplayName method assigns a display name to the current session.
helpviewer_keywords: ["IAudioSessionControl interface [Core Audio]","SetDisplayName method","IAudioSessionControl.SetDisplayName","IAudioSessionControl::SetDisplayName","IAudioSessionControlSetDisplayName","SetDisplayName","SetDisplayName method [Core Audio]","SetDisplayName method [Core Audio]","IAudioSessionControl interface","audiopolicy/IAudioSessionControl::SetDisplayName","coreaudio.iaudiosessioncontrol_setdisplayname"]
old-location: coreaudio\iaudiosessioncontrol_setdisplayname.htm
tech.root: CoreAudio
ms.assetid: d12c12ed-a556-4743-952e-2eb4f58ee0eb
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl interface [Core Audio],SetDisplayName method, IAudioSessionControl.SetDisplayName, IAudioSessionControl::SetDisplayName, IAudioSessionControlSetDisplayName, SetDisplayName, SetDisplayName method [Core Audio], SetDisplayName method [Core Audio],IAudioSessionControl interface, audiopolicy/IAudioSessionControl::SetDisplayName, coreaudio.iaudiosessioncontrol_setdisplayname
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
 - IAudioSessionControl::SetDisplayName
 - audiopolicy/IAudioSessionControl::SetDisplayName
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
 - IAudioSessionControl.SetDisplayName
---

# IAudioSessionControl::SetDisplayName


## -description

The <b>SetDisplayName</b> method assigns a display name to the current session.

## -parameters

### -param Value [in]

Pointer to a null-terminated, wide-character string that contains the display name for the session.

### -param EventContext [in]

Pointer to the event-context GUID. If a call to this method generates a name-change event, the session manager sends notifications to all clients that have registered <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interfaces with the session manager. The session manager includes the <i>EventContext</i> pointer value with each notification. Upon receiving a notification, a client can determine whether it or another client is the source of the event by inspecting the <i>EventContext</i> value. This scheme depends on the client selecting a value for this parameter that is unique among all clients in the session. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
Parameter <i>Value</i> is <b>NULL</b>.

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

In Windows Vista, the system-supplied program, Sndvol.exe, uses the display name to label the volume control for the session. If the client does not call <b>SetDisplayName</b> to assign a display name to the session, the Sndvol program uses a default, automatically generated name to label the session. The default name incorporates information such as the window title or version resource of the audio application.

If a client has more than one active session, client-specified display names are especially helpful for distinguishing among the volume controls for the various sessions.

In the case of a cross-process session, the session has no identifying information, such as an application name or process ID, from which to generate a default display name. Thus, the client must call <b>SetDisplayName</b> to avoid displaying a meaningless default display name.

The display name does not persist beyond the lifetime of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> object. Thus, after all references to the object are released, a subsequently created version of the object (with the same application, same session GUID, and same endpoint device) will once again have a default, automatically generated display name until the client calls <b>SetDisplayName</b>.

The client can retrieve the display name for the session by calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getdisplayname">IAudioSessionControl::GetDisplayName</a> method.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getdisplayname">IAudioSessionControl::GetDisplayName</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>