---
UID: NF:endpointvolume.IAudioEndpointVolume.SetMute
title: IAudioEndpointVolume::SetMute (endpointvolume.h)
description: The SetMute method sets the muting state of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","SetMute method","IAudioEndpointVolume.SetMute","IAudioEndpointVolume::SetMute","IAudioEndpointVolumeSetMute","SetMute","SetMute method [Core Audio]","SetMute method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_setmute","endpointvolume/IAudioEndpointVolume::SetMute"]
old-location: coreaudio\iaudioendpointvolume_setmute.htm
tech.root: CoreAudio
ms.assetid: a0ab4fef-8333-4f21-ae8e-74285788ae0e
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetMute method, IAudioEndpointVolume.SetMute, IAudioEndpointVolume::SetMute, IAudioEndpointVolumeSetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setmute, endpointvolume/IAudioEndpointVolume::SetMute
req.header: endpointvolume.h
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
 - IAudioEndpointVolume::SetMute
 - endpointvolume/IAudioEndpointVolume::SetMute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.SetMute
---

# IAudioEndpointVolume::SetMute


## -description

The <b>SetMute</b> method sets the muting state of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param bMute [in]

The new muting state. If <i>bMute</i> is <b>TRUE</b>, the method mutes the stream. If <b>FALSE</b>, the method turns off muting.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMute</b> call changes the muting state of the endpoint, all clients that have registered <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.

## -returns

If the method succeeds and the muting state changes, the method returns S_OK. If the method succeeds and the new muting state is the same as the previous muting state, the method returns S_FALSE. If the method fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

For a code example that calls <b>SetMute</b>, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>