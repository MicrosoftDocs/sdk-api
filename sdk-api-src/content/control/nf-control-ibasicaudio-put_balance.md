---
UID: NF:control.IBasicAudio.put_Balance
title: IBasicAudio::put_Balance (control.h)
description: The put_Balance method sets the balance of the audio signal.
helpviewer_keywords: ["IBasicAudio interface [DirectShow]","put_Balance method","IBasicAudio.put_Balance","IBasicAudio::put_Balance","IBasicAudioput_Balance","control/IBasicAudio::put_Balance","dshow.ibasicaudio_put_balance","put_Balance","put_Balance method [DirectShow]","put_Balance method [DirectShow]","IBasicAudio interface"]
old-location: dshow\ibasicaudio_put_balance.htm
tech.root: dshow
ms.assetid: 88cf4639-8f32-424f-a097-272c44592f6f
ms.date: 4/26/2023
ms.keywords: IBasicAudio interface [DirectShow],put_Balance method, IBasicAudio.put_Balance, IBasicAudio::put_Balance, IBasicAudioput_Balance, control/IBasicAudio::put_Balance, dshow.ibasicaudio_put_balance, put_Balance, put_Balance method [DirectShow], put_Balance method [DirectShow],IBasicAudio interface
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
 - IBasicAudio::put_Balance
 - control/IBasicAudio::put_Balance
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
 - IBasicAudio.put_Balance
---

# IBasicAudio::put_Balance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Balance</code> method sets the balance of the audio signal.

## -parameters

### -param lBalance [in]

Specifies the balance. The value can range from -10,000 to 10,000. The value -10,000 means the right channel is attenuated by 100 dB and is effectively silent. The value 10,000 means the left channel is silent. The neutral value is 0, which means that both channels are at full volume. When one channel is attenuated, the other remains at full volume.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The underlying audio device returned an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>lBalance</i> is invalid.

</td>
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