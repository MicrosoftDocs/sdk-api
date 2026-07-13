---
UID: NF:strmif.IAMTuner.put_CountryCode
title: IAMTuner::put_CountryCode (strmif.h)
description: The put_CountryCode method sets the country/region code to establish the frequency to use.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","put_CountryCode method","IAMTuner.put_CountryCode","IAMTuner::put_CountryCode","IAMTunerput_CountryCode","dshow.iamtuner_put_countrycode","put_CountryCode","put_CountryCode method [DirectShow]","put_CountryCode method [DirectShow]","IAMTuner interface","strmif/IAMTuner::put_CountryCode"]
old-location: dshow\iamtuner_put_countrycode.htm
tech.root: dshow
ms.assetid: d733f829-5600-4f75-9bc9-de8dc8dd8031
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],put_CountryCode method, IAMTuner.put_CountryCode, IAMTuner::put_CountryCode, IAMTunerput_CountryCode, dshow.iamtuner_put_countrycode, put_CountryCode, put_CountryCode method [DirectShow], put_CountryCode method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_CountryCode
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
 - IAMTuner::put_CountryCode
 - strmif/IAMTuner::put_CountryCode
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
 - IAMTuner.put_CountryCode
---

# IAMTuner::put_CountryCode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_CountryCode</code> method sets the country/region code to establish the frequency to use.

## -parameters

### -param lCountryCode [in]

Value indicating the country/region code.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method establishes the base frequencies for the given country/region. Use the <a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-autotune">IAMTVTuner::AutoTune</a> method to determine the exact frequencies for specific regions, unless there are previously cached settings for the new country/region.

Because channels in different countries/regions map to different frequencies, worldwide mapping tables are provided in the appendix <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>. Override the existing country/region code by selecting the new value from the appendix and passing it in as the parameter for the <code>put_CountryCode</code> method. This is useful when a country/region wants to receive broadcast video from a different national source.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>