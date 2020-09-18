---
UID: NF:mfidl.IMFAudioStreamVolume.SetAllVolumes
title: IMFAudioStreamVolume::SetAllVolumes (mfidl.h)
description: Sets the individual volume levels for all of the channels in the audio stream.
helpviewer_keywords: ["6c278693-5a2f-4aa2-b477-3b3014b2cc89","IMFAudioStreamVolume interface [Media Foundation]","SetAllVolumes method","IMFAudioStreamVolume.SetAllVolumes","IMFAudioStreamVolume::SetAllVolumes","SetAllVolumes","SetAllVolumes method [Media Foundation]","SetAllVolumes method [Media Foundation]","IMFAudioStreamVolume interface","mf.imfaudiostreamvolume_setallvolumes","mfidl/IMFAudioStreamVolume::SetAllVolumes"]
old-location: mf\imfaudiostreamvolume_setallvolumes.htm
tech.root: mf
ms.assetid: 6c278693-5a2f-4aa2-b477-3b3014b2cc89
ms.date: 12/05/2018
ms.keywords: 6c278693-5a2f-4aa2-b477-3b3014b2cc89, IMFAudioStreamVolume interface [Media Foundation],SetAllVolumes method, IMFAudioStreamVolume.SetAllVolumes, IMFAudioStreamVolume::SetAllVolumes, SetAllVolumes, SetAllVolumes method [Media Foundation], SetAllVolumes method [Media Foundation],IMFAudioStreamVolume interface, mf.imfaudiostreamvolume_setallvolumes, mfidl/IMFAudioStreamVolume::SetAllVolumes
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
 - IMFAudioStreamVolume::SetAllVolumes
 - mfidl/IMFAudioStreamVolume::SetAllVolumes
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
 - IMFAudioStreamVolume.SetAllVolumes
---

# IMFAudioStreamVolume::SetAllVolumes


## -description

Sets the individual volume levels for all of the channels in the audio stream.

## -parameters

### -param dwCount [in]

Number of elements in the <i>pfVolumes</i> array. The value must equal the number of channels. To get the number of channels, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfaudiostreamvolume-getchannelcount">IMFAudioStreamVolume::GetChannelCount</a>.

### -param pfVolumes [in]

Address of an array of size <i>dwCount</i>, allocated by the caller. The array specifies the volume levels for all of the channels. Before calling the method, set each element of the array to the desired volume level for the channel.

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