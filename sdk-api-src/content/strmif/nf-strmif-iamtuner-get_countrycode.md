---
UID: NF:strmif.IAMTuner.get_CountryCode
title: IAMTuner::get_CountryCode (strmif.h)
description: The get_CountryCode method retrieves the country/region code that establishes the current channel-to-frequency mapping.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","get_CountryCode method","IAMTuner.get_CountryCode","IAMTuner::get_CountryCode","IAMTunerget_CountryCode","dshow.iamtuner_get_countrycode","get_CountryCode","get_CountryCode method [DirectShow]","get_CountryCode method [DirectShow]","IAMTuner interface","strmif/IAMTuner::get_CountryCode"]
old-location: dshow\iamtuner_get_countrycode.htm
tech.root: dshow
ms.assetid: 8b459ad8-c9e0-4b35-aec4-113c8a67d907
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],get_CountryCode method, IAMTuner.get_CountryCode, IAMTuner::get_CountryCode, IAMTunerget_CountryCode, dshow.iamtuner_get_countrycode, get_CountryCode, get_CountryCode method [DirectShow], get_CountryCode method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_CountryCode
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
 - IAMTuner::get_CountryCode
 - strmif/IAMTuner::get_CountryCode
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
 - IAMTuner.get_CountryCode
---

# IAMTuner::get_CountryCode


## -description

The <code>get_CountryCode</code> method retrieves the country/region code that establishes the current channel-to-frequency mapping.

## -parameters

### -param plCountryCode [out]

Pointer to a variable that receives the country/region code currently in use by the <a href="/windows/desktop/DirectShow/tv-tuner-filter">TV Tuner</a> filter.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

The <a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-put_countrycode">IAMTuner::put_CountryCode</a> method determines which channel-to-frequency mapping table to use. This establishes the base frequencies for the given country/region. Use the <a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-autotune">IAMTVTuner::AutoTune</a> method to determine the exact frequencies for specific regions.

Override the country/region code when a country/region wants to receive broadcast video from a different national source. For a list of country/region codes, see <a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>