---
UID: NF:audiopolicy.IAudioSessionControl.SetGroupingParam
title: IAudioSessionControl::SetGroupingParam (audiopolicy.h)
description: The SetGroupingParam method assigns a session to a grouping of sessions.
helpviewer_keywords: ["IAudioSessionControl interface [Core Audio]","SetGroupingParam method","IAudioSessionControl.SetGroupingParam","IAudioSessionControl::SetGroupingParam","IAudioSessionControlSetGroupingParam","SetGroupingParam","SetGroupingParam method [Core Audio]","SetGroupingParam method [Core Audio]","IAudioSessionControl interface","audiopolicy/IAudioSessionControl::SetGroupingParam","coreaudio.iaudiosessioncontrol_setgroupingparam"]
old-location: coreaudio\iaudiosessioncontrol_setgroupingparam.htm
tech.root: CoreAudio
ms.assetid: 990bebd9-c37d-4f72-b349-a43a074d8992
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl interface [Core Audio],SetGroupingParam method, IAudioSessionControl.SetGroupingParam, IAudioSessionControl::SetGroupingParam, IAudioSessionControlSetGroupingParam, SetGroupingParam, SetGroupingParam method [Core Audio], SetGroupingParam method [Core Audio],IAudioSessionControl interface, audiopolicy/IAudioSessionControl::SetGroupingParam, coreaudio.iaudiosessioncontrol_setgroupingparam
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
 - IAudioSessionControl::SetGroupingParam
 - audiopolicy/IAudioSessionControl::SetGroupingParam
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
 - IAudioSessionControl.SetGroupingParam
---

# IAudioSessionControl::SetGroupingParam


## -description

The <b>SetGroupingParam</b> method assigns a session to a grouping of sessions.

## -parameters

### -param Override [in]

The new grouping parameter. This parameter must be a valid, non-<b>NULL</b> pointer to a grouping-parameter GUID. For more information, see Remarks.

### -param EventContext [in]

Pointer to the event-context GUID. If a call to this method generates a grouping-change event, the session manager sends notifications to all clients that have registered <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interfaces with the session manager. The session manager includes the <i>EventContext</i> pointer value with each notification. Upon receiving a notification, a client can determine whether it or another client is the source of the event by inspecting the <i>EventContext</i> value. This scheme depends on the client selecting a value for this parameter that is unique among all clients in the session. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
Parameter <i>Grouping</i> is <b>NULL</b>.

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

A client calls this method to change the grouping parameter of a session. All of the audio sessions that have the same grouping parameter value are under the control of the same volume-level slider in the system volume-control program, Sndvol. For more information, see <a href="/windows/desktop/CoreAudio/grouping-parameters">Grouping Parameters</a>.

The client can get the current grouping parameter for the session by calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam">IAudioSessionControl::GetGroupingParam</a> method.

If a client has never called <b>SetGroupingParam</b> to assign a grouping parameter to a session, the session does not belong to any grouping. A session that does not belong to any grouping has its own, dedicated volume-level slider in the Sndvol program.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam">IAudioSessionControl::GetGroupingParam</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>