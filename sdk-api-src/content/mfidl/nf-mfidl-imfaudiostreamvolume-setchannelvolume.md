---
UID: NF:mfidl.IMFAudioStreamVolume.SetChannelVolume
title: IMFAudioStreamVolume::SetChannelVolume (mfidl.h)
description: Sets the volume level for a specified channel in the audio stream.
helpviewer_keywords: ["7786a6aa-c777-4b65-b38c-a75cd654a080","IMFAudioStreamVolume interface [Media Foundation]","SetChannelVolume method","IMFAudioStreamVolume.SetChannelVolume","IMFAudioStreamVolume::SetChannelVolume","SetChannelVolume","SetChannelVolume method [Media Foundation]","SetChannelVolume method [Media Foundation]","IMFAudioStreamVolume interface","mf.imfaudiostreamvolume_setchannelvolume","mfidl/IMFAudioStreamVolume::SetChannelVolume"]
old-location: mf\imfaudiostreamvolume_setchannelvolume.htm
tech.root: mf
ms.assetid: 7786a6aa-c777-4b65-b38c-a75cd654a080
ms.date: 12/05/2018
ms.keywords: 7786a6aa-c777-4b65-b38c-a75cd654a080, IMFAudioStreamVolume interface [Media Foundation],SetChannelVolume method, IMFAudioStreamVolume.SetChannelVolume, IMFAudioStreamVolume::SetChannelVolume, SetChannelVolume, SetChannelVolume method [Media Foundation], SetChannelVolume method [Media Foundation],IMFAudioStreamVolume interface, mf.imfaudiostreamvolume_setchannelvolume, mfidl/IMFAudioStreamVolume::SetChannelVolume
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
 - IMFAudioStreamVolume::SetChannelVolume
 - mfidl/IMFAudioStreamVolume::SetChannelVolume
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
 - IMFAudioStreamVolume.SetChannelVolume
---

# IMFAudioStreamVolume::SetChannelVolume


## -description

Sets the volume level for a specified channel in the audio stream.

## -parameters

### -param dwIndex [in]

Zero-based index of the audio channel. To get the number of channels, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelcount">IMFAudioStreamVolume::GetChannelCount</a>.

### -param fLevel [in]

Volume level for the channel.

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