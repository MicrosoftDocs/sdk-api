---
UID: NF:mfidl.IMFAudioStreamVolume.GetChannelCount
title: IMFAudioStreamVolume::GetChannelCount (mfidl.h)
description: Retrieves the number of channels in the audio stream.
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Media Foundation]","GetChannelCount method [Media Foundation]","IMFAudioStreamVolume interface","IMFAudioStreamVolume interface [Media Foundation]","GetChannelCount method","IMFAudioStreamVolume.GetChannelCount","IMFAudioStreamVolume::GetChannelCount","d19a56db-cd5f-4a19-98f0-42327c259b01","mf.imfaudiostreamvolume_getchannelcount","mfidl/IMFAudioStreamVolume::GetChannelCount"]
old-location: mf\imfaudiostreamvolume_getchannelcount.htm
tech.root: mf
ms.assetid: d19a56db-cd5f-4a19-98f0-42327c259b01
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Media Foundation], GetChannelCount method [Media Foundation],IMFAudioStreamVolume interface, IMFAudioStreamVolume interface [Media Foundation],GetChannelCount method, IMFAudioStreamVolume.GetChannelCount, IMFAudioStreamVolume::GetChannelCount, d19a56db-cd5f-4a19-98f0-42327c259b01, mf.imfaudiostreamvolume_getchannelcount, mfidl/IMFAudioStreamVolume::GetChannelCount
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
 - IMFAudioStreamVolume::GetChannelCount
 - mfidl/IMFAudioStreamVolume::GetChannelCount
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
 - IMFAudioStreamVolume.GetChannelCount
---

# IMFAudioStreamVolume::GetChannelCount


## -description

Retrieves the number of channels in the audio stream.

## -parameters

### -param pdwCount [out]

Receives the number of channels in the audio stream.

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