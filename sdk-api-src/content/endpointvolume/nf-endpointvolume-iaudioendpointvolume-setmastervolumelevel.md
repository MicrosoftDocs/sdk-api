---
UID: NF:endpointvolume.IAudioEndpointVolume.SetMasterVolumeLevel
title: IAudioEndpointVolume::SetMasterVolumeLevel (endpointvolume.h)
description: The SetMasterVolumeLevel method sets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","SetMasterVolumeLevel method","IAudioEndpointVolume.SetMasterVolumeLevel","IAudioEndpointVolume::SetMasterVolumeLevel","IAudioEndpointVolumeSetMasterVolumeLevel","SetMasterVolumeLevel","SetMasterVolumeLevel method [Core Audio]","SetMasterVolumeLevel method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_setmastervolumelevel","endpointvolume/IAudioEndpointVolume::SetMasterVolumeLevel"]
old-location: coreaudio\iaudioendpointvolume_setmastervolumelevel.htm
tech.root: CoreAudio
ms.assetid: 776d7667-f48b-44c0-9441-177b86b52da9
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetMasterVolumeLevel method, IAudioEndpointVolume.SetMasterVolumeLevel, IAudioEndpointVolume::SetMasterVolumeLevel, IAudioEndpointVolumeSetMasterVolumeLevel, SetMasterVolumeLevel, SetMasterVolumeLevel method [Core Audio], SetMasterVolumeLevel method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setmastervolumelevel, endpointvolume/IAudioEndpointVolume::SetMasterVolumeLevel
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
 - IAudioEndpointVolume::SetMasterVolumeLevel
 - endpointvolume/IAudioEndpointVolume::SetMasterVolumeLevel
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
 - IAudioEndpointVolume.SetMasterVolumeLevel
---

# IAudioEndpointVolume::SetMasterVolumeLevel


## -description

The <b>SetMasterVolumeLevel</b> method sets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param fLevelDB [in]

The new master volume level in decibels. To obtain the range and granularity of the volume levels that can be set by this method, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> method.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMasterVolumeLevel</b> call changes the volume level of the endpoint, all clients that have registered <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.

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
Parameter <i>fLevelDB</i> lies outside of the volume range supported by the device.

</td>
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

If volume level <i>fLevelDB</i> falls outside of the volume range reported by the <b>IAudioEndpointVolume::GetVolumeRange</b> method, the <b>SetMasterVolumeLevel</b> call fails and returns error code E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>