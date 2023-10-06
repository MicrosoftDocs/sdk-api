---
UID: NF:control.IBasicAudio.get_Balance
title: IBasicAudio::get_Balance (control.h)
description: The get_Balance method retrieves the balance for the audio signal.
helpviewer_keywords: ["IBasicAudio interface [DirectShow]","get_Balance method","IBasicAudio.get_Balance","IBasicAudio::get_Balance","IBasicAudioget_Balance","control/IBasicAudio::get_Balance","dshow.ibasicaudio_get_balance","get_Balance","get_Balance method [DirectShow]","get_Balance method [DirectShow]","IBasicAudio interface"]
old-location: dshow\ibasicaudio_get_balance.htm
tech.root: dshow
ms.assetid: bb9796c5-0dd2-496a-b5b4-a6614d7770c1
ms.date: 4/26/2023
ms.keywords: IBasicAudio interface [DirectShow],get_Balance method, IBasicAudio.get_Balance, IBasicAudio::get_Balance, IBasicAudioget_Balance, control/IBasicAudio::get_Balance, dshow.ibasicaudio_get_balance, get_Balance, get_Balance method [DirectShow], get_Balance method [DirectShow],IBasicAudio interface
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
 - IBasicAudio::get_Balance
 - control/IBasicAudio::get_Balance
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
 - IBasicAudio.get_Balance
---

# IBasicAudio::get_Balance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Balance</code> method retrieves the balance for the audio signal.

## -parameters

### -param plBalance [out]

Pointer to a variable that receives the balance.

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

## -remarks

The balance ranges from -10,000 to 10,000. The value -10,000 means the right channel is attenuated by 100 dB and is effectively silent. The value 10,000 means the left channel is silent. The neutral value is 0, which means that both channels are at full volume. When one channel is attenuated, the other remains at full volume.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicaudio">IBasicAudio Interface</a>