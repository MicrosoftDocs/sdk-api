---
UID: NF:control.IBasicAudio.get_Volume
title: IBasicAudio::get_Volume (control.h)
description: The get_Volume method retrieves the volume (amplitude) of the audio signal.
helpviewer_keywords: ["IBasicAudio interface [DirectShow]","get_Volume method","IBasicAudio.get_Volume","IBasicAudio::get_Volume","IBasicAudioget_Volume","control/IBasicAudio::get_Volume","dshow.ibasicaudio_get_volume","get_Volume","get_Volume method [DirectShow]","get_Volume method [DirectShow]","IBasicAudio interface"]
old-location: dshow\ibasicaudio_get_volume.htm
tech.root: dshow
ms.assetid: 3258da5a-ab44-4c8a-813b-79a0c28693a3
ms.date: 4/26/2023
ms.keywords: IBasicAudio interface [DirectShow],get_Volume method, IBasicAudio.get_Volume, IBasicAudio::get_Volume, IBasicAudioget_Volume, control/IBasicAudio::get_Volume, dshow.ibasicaudio_get_volume, get_Volume, get_Volume method [DirectShow], get_Volume method [DirectShow],IBasicAudio interface
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicAudio::get_Volume
 - control/IBasicAudio::get_Volume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicAudio.get_Volume
---

# IBasicAudio::get_Volume


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Volume</code> method retrieves the volume (amplitude) of the audio signal.

## -parameters

### -param plVolume [out]

Pointer to a variable that receive the volume. Divide by 100 to get equivalent decibel value. For example, –10,000 is –100 dB.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The filter graph does not contain an audio renderer filter. (Possibly the source does not contain an audio stream.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicaudio">IBasicAudio Interface</a>