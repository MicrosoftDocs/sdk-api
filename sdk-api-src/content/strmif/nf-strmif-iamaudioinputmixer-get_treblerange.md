---
UID: NF:strmif.IAMAudioInputMixer.get_TrebleRange
title: IAMAudioInputMixer::get_TrebleRange (strmif.h)
description: The get_TrebleRange method retrieves the treble range for this input.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_TrebleRange method","IAMAudioInputMixer.get_TrebleRange","IAMAudioInputMixer::get_TrebleRange","IAMAudioInputMixerget_TrebleRange","dshow.iamaudioinputmixer_get_treblerange","get_TrebleRange","get_TrebleRange method [DirectShow]","get_TrebleRange method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_TrebleRange"]
old-location: dshow\iamaudioinputmixer_get_treblerange.htm
tech.root: dshow
ms.assetid: 726cbdda-5772-43bc-846f-f7d1672cc56f
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_TrebleRange method, IAMAudioInputMixer.get_TrebleRange, IAMAudioInputMixer::get_TrebleRange, IAMAudioInputMixerget_TrebleRange, dshow.iamaudioinputmixer_get_treblerange, get_TrebleRange, get_TrebleRange method [DirectShow], get_TrebleRange method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_TrebleRange
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
 - IAMAudioInputMixer::get_TrebleRange
 - strmif/IAMAudioInputMixer::get_TrebleRange
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
 - IAMAudioInputMixer.get_TrebleRange
---

# IAMAudioInputMixer::get_TrebleRange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_TrebleRange</code> method retrieves the treble range for this input.

## -parameters

### -param pRange [out]

Receives the largest valid value for the <a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_treble">IAMAudioInputMixer::put_Treble</a>. For example, 6.0 means that any value between –6.0 and 6.0 is valid.

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_treble">IAMAudioInputMixer::put_Treble</a>