---
UID: NF:strmif.IAMAudioInputMixer.get_Pan
title: IAMAudioInputMixer::get_Pan (strmif.h)
description: The get_Pan method retrieves the pan level.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Pan method","IAMAudioInputMixer.get_Pan","IAMAudioInputMixer::get_Pan","IAMAudioInputMixerget_Pan","dshow.iamaudioinputmixer_get_pan","get_Pan","get_Pan method [DirectShow]","get_Pan method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Pan"]
old-location: dshow\iamaudioinputmixer_get_pan.htm
tech.root: dshow
ms.assetid: aa1aae16-484e-4f78-901e-2fdb0d8e365c
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Pan method, IAMAudioInputMixer.get_Pan, IAMAudioInputMixer::get_Pan, IAMAudioInputMixerget_Pan, dshow.iamaudioinputmixer_get_pan, get_Pan, get_Pan method [DirectShow], get_Pan method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Pan
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
 - IAMAudioInputMixer::get_Pan
 - strmif/IAMAudioInputMixer::get_Pan
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
 - IAMAudioInputMixer.get_Pan
---

# IAMAudioInputMixer::get_Pan


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Pan</code> method retrieves the pan level.

## -parameters

### -param pPan [out]

Receives the pan level. Possible values range from –1.0 to 1.0, as follows:

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_pan">IAMAudioInputMixer::put_Pan</a>