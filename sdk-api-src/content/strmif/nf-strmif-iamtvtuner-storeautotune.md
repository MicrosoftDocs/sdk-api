---
UID: NF:strmif.IAMTVTuner.StoreAutoTune
title: IAMTVTuner::StoreAutoTune (strmif.h)
description: The StoreAutoTune method saves the fine-tuning information for all channels.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","StoreAutoTune method","IAMTVTuner.StoreAutoTune","IAMTVTuner::StoreAutoTune","IAMTVTunerStoreAutoTune","StoreAutoTune","StoreAutoTune method [DirectShow]","StoreAutoTune method [DirectShow]","IAMTVTuner interface","dshow.iamtvtuner_storeautotune","strmif/IAMTVTuner::StoreAutoTune"]
old-location: dshow\iamtvtuner_storeautotune.htm
tech.root: dshow
ms.assetid: 6e39d757-d8bd-4011-9a67-6bf57b5d820b
ms.date: 4/26/2023
ms.keywords: IAMTVTuner interface [DirectShow],StoreAutoTune method, IAMTVTuner.StoreAutoTune, IAMTVTuner::StoreAutoTune, IAMTVTunerStoreAutoTune, StoreAutoTune, StoreAutoTune method [DirectShow], StoreAutoTune method [DirectShow],IAMTVTuner interface, dshow.iamtvtuner_storeautotune, strmif/IAMTVTuner::StoreAutoTune
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
 - IAMTVTuner::StoreAutoTune
 - strmif/IAMTVTuner::StoreAutoTune
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
 - IAMTVTuner.StoreAutoTune
---

# IAMTVTuner::StoreAutoTune


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StoreAutoTune</code> method saves the fine-tuning information for all channels.



## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Override the channel-to-frequency information stored by this method by setting a new country/region code in the <a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-put_countrycode">IAMTuner::put_CountryCode</a> method. For a listing of country/region codes, see <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
