---
UID: NF:endpointvolume.IAudioEndpointVolume.GetChannelCount
title: IAudioEndpointVolume::GetChannelCount (endpointvolume.h)
description: The GetChannelCount method gets a count of the channels in the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Core Audio]","GetChannelCount method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetChannelCount method","IAudioEndpointVolume.GetChannelCount","IAudioEndpointVolume::GetChannelCount","IAudioEndpointVolumeGetChannelCount","coreaudio.iaudioendpointvolume_getchannelcount","endpointvolume/IAudioEndpointVolume::GetChannelCount"]
old-location: coreaudio\iaudioendpointvolume_getchannelcount.htm
tech.root: CoreAudio
ms.assetid: 83fd9afe-9bca-4569-a705-0e366b56522e
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Core Audio], GetChannelCount method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetChannelCount method, IAudioEndpointVolume.GetChannelCount, IAudioEndpointVolume::GetChannelCount, IAudioEndpointVolumeGetChannelCount, coreaudio.iaudioendpointvolume_getchannelcount, endpointvolume/IAudioEndpointVolume::GetChannelCount
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
 - IAudioEndpointVolume::GetChannelCount
 - endpointvolume/IAudioEndpointVolume::GetChannelCount
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
 - IAudioEndpointVolume.GetChannelCount
---

# IAudioEndpointVolume::GetChannelCount


## -description

The <b>GetChannelCount</b> method gets a count of the channels in the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param pnChannelCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the channel count.

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
Parameter <i>pnChannelCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>