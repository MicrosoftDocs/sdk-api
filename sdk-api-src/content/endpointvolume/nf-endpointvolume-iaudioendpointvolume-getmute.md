---
UID: NF:endpointvolume.IAudioEndpointVolume.GetMute
title: IAudioEndpointVolume::GetMute (endpointvolume.h)
description: The GetMute method gets the muting state of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetMute","GetMute method [Core Audio]","GetMute method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetMute method","IAudioEndpointVolume.GetMute","IAudioEndpointVolume::GetMute","IAudioEndpointVolumeGetMute","coreaudio.iaudioendpointvolume_getmute","endpointvolume/IAudioEndpointVolume::GetMute"]
old-location: coreaudio\iaudioendpointvolume_getmute.htm
tech.root: CoreAudio
ms.assetid: bb7cbb42-74cd-4951-92b1-a76ca42e5d3a
ms.date: 12/05/2018
ms.keywords: GetMute, GetMute method [Core Audio], GetMute method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetMute method, IAudioEndpointVolume.GetMute, IAudioEndpointVolume::GetMute, IAudioEndpointVolumeGetMute, coreaudio.iaudioendpointvolume_getmute, endpointvolume/IAudioEndpointVolume::GetMute
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
 - IAudioEndpointVolume::GetMute
 - endpointvolume/IAudioEndpointVolume::GetMute
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
 - IAudioEndpointVolume.GetMute
---

# IAudioEndpointVolume::GetMute


## -description

The <b>GetMute</b> method gets the muting state of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param pbMute [out]

Pointer to a <b>BOOL</b> variable into which the method writes the muting state. If <i>*pbMute</i> is <b>TRUE</b>, the stream is muted. If <b>FALSE</b>, the stream is not muted.

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
Parameter <i>pbMute</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For a code example that calls <b>GetMute</b>, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>