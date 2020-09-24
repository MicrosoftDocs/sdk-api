---
UID: NF:endpointvolume.IAudioEndpointVolume.GetMasterVolumeLevel
title: IAudioEndpointVolume::GetMasterVolumeLevel (endpointvolume.h)
description: The GetMasterVolumeLevel method gets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["GetMasterVolumeLevel","GetMasterVolumeLevel method [Core Audio]","GetMasterVolumeLevel method [Core Audio]","IAudioEndpointVolume interface","IAudioEndpointVolume interface [Core Audio]","GetMasterVolumeLevel method","IAudioEndpointVolume.GetMasterVolumeLevel","IAudioEndpointVolume::GetMasterVolumeLevel","IAudioEndpointVolumeGetMasterVolumeLevel","coreaudio.iaudioendpointvolume_getmastervolumelevel","endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevel"]
old-location: coreaudio\iaudioendpointvolume_getmastervolumelevel.htm
tech.root: CoreAudio
ms.assetid: 26e208e1-2291-4db6-857d-00b25d8fa343
ms.date: 12/05/2018
ms.keywords: GetMasterVolumeLevel, GetMasterVolumeLevel method [Core Audio], GetMasterVolumeLevel method [Core Audio],IAudioEndpointVolume interface, IAudioEndpointVolume interface [Core Audio],GetMasterVolumeLevel method, IAudioEndpointVolume.GetMasterVolumeLevel, IAudioEndpointVolume::GetMasterVolumeLevel, IAudioEndpointVolumeGetMasterVolumeLevel, coreaudio.iaudioendpointvolume_getmastervolumelevel, endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevel
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
 - IAudioEndpointVolume::GetMasterVolumeLevel
 - endpointvolume/IAudioEndpointVolume::GetMasterVolumeLevel
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
 - IAudioEndpointVolume.GetMasterVolumeLevel
---

# IAudioEndpointVolume::GetMasterVolumeLevel


## -description

The <b>GetMasterVolumeLevel</b> method gets the master volume level, in decibels, of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param pfLevelDB [out]

Pointer to the master volume level. This parameter points to a <b>float</b> variable into which the method writes the volume level in decibels. To get the range of volume levels obtained from this method, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> method.

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
Parameter <i>pfLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a>