---
UID: NF:mfidl.IMFAudioStreamVolume.GetAllVolumes
title: IMFAudioStreamVolume::GetAllVolumes (mfidl.h)
description: Retrieves the volume levels for all of the channels in the audio stream.
helpviewer_keywords: ["GetAllVolumes","GetAllVolumes method [Media Foundation]","GetAllVolumes method [Media Foundation]","IMFAudioStreamVolume interface","IMFAudioStreamVolume interface [Media Foundation]","GetAllVolumes method","IMFAudioStreamVolume.GetAllVolumes","IMFAudioStreamVolume::GetAllVolumes","cbcc0b5b-a60d-49ca-8b1c-7104e039a7d2","mf.imfaudiostreamvolume_getallvolumes","mfidl/IMFAudioStreamVolume::GetAllVolumes"]
old-location: mf\imfaudiostreamvolume_getallvolumes.htm
tech.root: mf
ms.assetid: cbcc0b5b-a60d-49ca-8b1c-7104e039a7d2
ms.date: 12/05/2018
ms.keywords: GetAllVolumes, GetAllVolumes method [Media Foundation], GetAllVolumes method [Media Foundation],IMFAudioStreamVolume interface, IMFAudioStreamVolume interface [Media Foundation],GetAllVolumes method, IMFAudioStreamVolume.GetAllVolumes, IMFAudioStreamVolume::GetAllVolumes, cbcc0b5b-a60d-49ca-8b1c-7104e039a7d2, mf.imfaudiostreamvolume_getallvolumes, mfidl/IMFAudioStreamVolume::GetAllVolumes
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
 - IMFAudioStreamVolume::GetAllVolumes
 - mfidl/IMFAudioStreamVolume::GetAllVolumes
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
 - IMFAudioStreamVolume.GetAllVolumes
---

# IMFAudioStreamVolume::GetAllVolumes


## -description

Retrieves the volume levels for all of the channels in the audio stream.

## -parameters

### -param dwCount [in]

Number of elements in the <i>pfVolumes</i> array. The value must equal the number of channels. To get the number of channels, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelcount">IMFAudioStreamVolume::GetChannelCount</a>.

### -param pfVolumes [out]

Address of an array of size <i>dwCount</i>, allocated by the caller. The method fills the array with the volume level for each channel in the stream.

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