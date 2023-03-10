---
UID: NF:endpointvolume.IAudioEndpointVolumeEx.GetVolumeRangeChannel
title: IAudioEndpointVolumeEx::GetVolumeRangeChannel (endpointvolume.h)
description: The GetVolumeRangeChannel method gets the volume range for a specified channel.
helpviewer_keywords: ["GetVolumeRangeChannel","GetVolumeRangeChannel method [Core Audio]","GetVolumeRangeChannel method [Core Audio]","IAudioEndpointVolumeEx interface","IAudioEndpointVolumeEx interface [Core Audio]","GetVolumeRangeChannel method","IAudioEndpointVolumeEx.GetVolumeRangeChannel","IAudioEndpointVolumeEx::GetVolumeRangeChannel","coreaudio.iaudioendpointvolumeex_getvolumerangechannel","endpointvolume/IAudioEndpointVolumeEx::GetVolumeRangeChannel"]
old-location: coreaudio\iaudioendpointvolumeex_getvolumerangechannel.htm
tech.root: CoreAudio
ms.assetid: 869fe1cc-aa32-45e5-899f-3ae0d0f1b256
ms.date: 12/05/2018
ms.keywords: GetVolumeRangeChannel, GetVolumeRangeChannel method [Core Audio], GetVolumeRangeChannel method [Core Audio],IAudioEndpointVolumeEx interface, IAudioEndpointVolumeEx interface [Core Audio],GetVolumeRangeChannel method, IAudioEndpointVolumeEx.GetVolumeRangeChannel, IAudioEndpointVolumeEx::GetVolumeRangeChannel, coreaudio.iaudioendpointvolumeex_getvolumerangechannel, endpointvolume/IAudioEndpointVolumeEx::GetVolumeRangeChannel
req.header: endpointvolume.h
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
 - IAudioEndpointVolumeEx::GetVolumeRangeChannel
 - endpointvolume/IAudioEndpointVolumeEx::GetVolumeRangeChannel
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
 - IAudioEndpointVolumeEx.GetVolumeRangeChannel
---

# IAudioEndpointVolumeEx::GetVolumeRangeChannel


## -description

The <b>GetVolumeRangeChannel</b> method gets the volume range for a specified channel.

## -parameters

### -param iChannel [in]

The channel number for which to get the volume range. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels in the stream, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a> method.

### -param pflVolumeMindB [out]

Receives  the minimum volume level for the channel, in decibels.

### -param pflVolumeMaxdB [out]

Receives  the maximum volume level for the channel, in decibels.

### -param pflVolumeIncrementdB [out]

Receives the volume increment for the channel, in decibels.

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
Parameter <i>pfLevelMinDB</i>, <i>pfLevelMaxDB</i>, or <i>pfVolumeIncrementDB</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumeex">IAudioEndpointVolumeEx</a>