---
UID: NF:strmif.IAMTVTuner.get_AudioFrequency
title: IAMTVTuner::get_AudioFrequency (strmif.h)
description: The get_AudioFrequency method retrieves the currently tuned audio frequency.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_AudioFrequency method","IAMTVTuner.get_AudioFrequency","IAMTVTuner::get_AudioFrequency","IAMTVTunerget_AudioFrequency","dshow.iamtvtuner_get_audiofrequency","get_AudioFrequency","get_AudioFrequency method [DirectShow]","get_AudioFrequency method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_AudioFrequency"]
old-location: dshow\iamtvtuner_get_audiofrequency.htm
tech.root: dshow
ms.assetid: 7d0d288a-7ad0-40ad-b86e-9df9447ed484
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_AudioFrequency method, IAMTVTuner.get_AudioFrequency, IAMTVTuner::get_AudioFrequency, IAMTVTunerget_AudioFrequency, dshow.iamtvtuner_get_audiofrequency, get_AudioFrequency, get_AudioFrequency method [DirectShow], get_AudioFrequency method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_AudioFrequency
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
 - IAMTVTuner::get_AudioFrequency
 - strmif/IAMTVTuner::get_AudioFrequency
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
 - IAMTVTuner.get_AudioFrequency
---

# IAMTVTuner::get_AudioFrequency


## -description

The <code>get_AudioFrequency</code> method retrieves the currently tuned audio frequency.

## -parameters

### -param lFreq [out]

Pointer to a variable that receives the audio frequency, in hertz (Hz).

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This is a diagnostic method that enables you to examine the exact frequency being used for a given channel.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>