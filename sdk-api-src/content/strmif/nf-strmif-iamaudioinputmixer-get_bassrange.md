---
UID: NF:strmif.IAMAudioInputMixer.get_BassRange
title: IAMAudioInputMixer::get_BassRange (strmif.h)
description: The get_BassRange method retrieves the bass range.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_BassRange method","IAMAudioInputMixer.get_BassRange","IAMAudioInputMixer::get_BassRange","IAMAudioInputMixerget_BassRange","dshow.iamaudioinputmixer_get_bassrange","get_BassRange","get_BassRange method [DirectShow]","get_BassRange method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_BassRange"]
old-location: dshow\iamaudioinputmixer_get_bassrange.htm
tech.root: dshow
ms.assetid: e0a77f8c-8608-4e16-bc7a-3c90dde2aad8
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_BassRange method, IAMAudioInputMixer.get_BassRange, IAMAudioInputMixer::get_BassRange, IAMAudioInputMixerget_BassRange, dshow.iamaudioinputmixer_get_bassrange, get_BassRange, get_BassRange method [DirectShow], get_BassRange method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_BassRange
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
 - IAMAudioInputMixer::get_BassRange
 - strmif/IAMAudioInputMixer::get_BassRange
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
 - IAMAudioInputMixer.get_BassRange
---

# IAMAudioInputMixer::get_BassRange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_BassRange</code> method retrieves the bass range.

## -parameters

### -param pRange [out]

Receives the largest valid value for the <a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_bass">IAMAudioInputMixer::put_Bass</a> method. For example, 6.0 means that any value between –6.0 and 6.0 is valid.

## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_bass">IAMAudioInputMixer::put_Bass</a>