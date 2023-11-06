---
UID: NF:strmif.IAMAudioInputMixer.put_Pan
title: IAMAudioInputMixer::put_Pan (strmif.h)
description: The put_Pan method sets the pan level.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Pan method","IAMAudioInputMixer.put_Pan","IAMAudioInputMixer::put_Pan","IAMAudioInputMixerput_Pan","dshow.iamaudioinputmixer_put_pan","put_Pan","put_Pan method [DirectShow]","put_Pan method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Pan"]
old-location: dshow\iamaudioinputmixer_put_pan.htm
tech.root: dshow
ms.assetid: eb0528e0-81d0-45a3-831a-8cf3ff1232b6
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Pan method, IAMAudioInputMixer.put_Pan, IAMAudioInputMixer::put_Pan, IAMAudioInputMixerput_Pan, dshow.iamaudioinputmixer_put_pan, put_Pan, put_Pan method [DirectShow], put_Pan method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Pan
req.header: strmif.h
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
 - IAMAudioInputMixer::put_Pan
 - strmif/IAMAudioInputMixer::put_Pan
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
 - IAMAudioInputMixer.put_Pan
---

# IAMAudioInputMixer::put_Pan


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Pan</code> method sets the pan level.

## -parameters

### -param Pan [in]

Specifies the pan level. Possible values range from –1.0 to 1.0, as follows.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>-1</td>
<td>Full left</td>
</tr>
<tr>
<td>0</td>
<td>Center</td>
</tr>
<tr>
<td>1</td>
<td>Full right</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

In a stereo recording, setting the pan level to -1.0 or 1.0 sends the entire signal to one channel. The other channel records silence. Panning has no effect for a mono recording.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_pan">IAMAudioInputMixer::get_Pan</a>