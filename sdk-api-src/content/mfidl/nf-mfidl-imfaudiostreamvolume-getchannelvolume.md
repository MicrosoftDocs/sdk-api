---
UID: NF:mfidl.IMFAudioStreamVolume.GetChannelVolume
title: IMFAudioStreamVolume::GetChannelVolume (mfidl.h)
description: Retrieves the volume level for a specified channel in the audio stream.
helpviewer_keywords: ["5cfcc3a8-2911-45a3-8322-bf4e3b023dd2","GetChannelVolume","GetChannelVolume method [Media Foundation]","GetChannelVolume method [Media Foundation]","IMFAudioStreamVolume interface","IMFAudioStreamVolume interface [Media Foundation]","GetChannelVolume method","IMFAudioStreamVolume.GetChannelVolume","IMFAudioStreamVolume::GetChannelVolume","mf.imfaudiostreamvolume_getchannelvolume","mfidl/IMFAudioStreamVolume::GetChannelVolume"]
old-location: mf\imfaudiostreamvolume_getchannelvolume.htm
tech.root: mf
ms.assetid: 5cfcc3a8-2911-45a3-8322-bf4e3b023dd2
ms.date: 12/05/2018
ms.keywords: 5cfcc3a8-2911-45a3-8322-bf4e3b023dd2, GetChannelVolume, GetChannelVolume method [Media Foundation], GetChannelVolume method [Media Foundation],IMFAudioStreamVolume interface, IMFAudioStreamVolume interface [Media Foundation],GetChannelVolume method, IMFAudioStreamVolume.GetChannelVolume, IMFAudioStreamVolume::GetChannelVolume, mf.imfaudiostreamvolume_getchannelvolume, mfidl/IMFAudioStreamVolume::GetChannelVolume
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAudioStreamVolume::GetChannelVolume
 - mfidl/IMFAudioStreamVolume::GetChannelVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioStreamVolume.GetChannelVolume
---

# IMFAudioStreamVolume::GetChannelVolume


## -description

Retrieves the volume level for a specified channel in the audio stream.

## -parameters

### -param dwIndex [in]

Zero-based index of the audio channel. To get the number of channels, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelcount">IMFAudioStreamVolume::GetChannelCount</a>.

### -param pfLevel [out]

Receives the volume level for the channel.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume">IMFAudioStreamVolume</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>