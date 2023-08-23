---
UID: NF:strmif.IAMTuner.get_TuningSpace
title: IAMTuner::get_TuningSpace (strmif.h)
description: The get_TuningSpace method retrieves the tuning space.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","get_TuningSpace method","IAMTuner.get_TuningSpace","IAMTuner::get_TuningSpace","IAMTunerget_TuningSpace","dshow.iamtuner_get_tuningspace","get_TuningSpace","get_TuningSpace method [DirectShow]","get_TuningSpace method [DirectShow]","IAMTuner interface","strmif/IAMTuner::get_TuningSpace"]
old-location: dshow\iamtuner_get_tuningspace.htm
tech.root: dshow
ms.assetid: 838451c2-2e0b-4a41-a512-f44283573ee6
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],get_TuningSpace method, IAMTuner.get_TuningSpace, IAMTuner::get_TuningSpace, IAMTunerget_TuningSpace, dshow.iamtuner_get_tuningspace, get_TuningSpace, get_TuningSpace method [DirectShow], get_TuningSpace method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_TuningSpace
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
 - IAMTuner::get_TuningSpace
 - strmif/IAMTuner::get_TuningSpace
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
 - IAMTuner.get_TuningSpace
---

# IAMTuner::get_TuningSpace


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_TuningSpace</code> method retrieves the tuning space.

## -parameters

### -param plTuningSpace [out]

Pointer to a variable that receives the current tuning space.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The application defines the value retrieved by this method; it is set through a call to <a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-put_tuningspace">IAMTuner::put_TuningSpace</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>