---
UID: NF:strmif.IAMTVTuner.get_VideoFrequency
title: IAMTVTuner::get_VideoFrequency (strmif.h)
description: The get_VideoFrequency method retrieves the current video frequency.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_VideoFrequency method","IAMTVTuner.get_VideoFrequency","IAMTVTuner::get_VideoFrequency","IAMTVTunerget_VideoFrequency","dshow.iamtvtuner_get_videofrequency","get_VideoFrequency","get_VideoFrequency method [DirectShow]","get_VideoFrequency method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_VideoFrequency"]
old-location: dshow\iamtvtuner_get_videofrequency.htm
tech.root: dshow
ms.assetid: d19552ce-1314-4217-9bd3-72369b4334cf
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_VideoFrequency method, IAMTVTuner.get_VideoFrequency, IAMTVTuner::get_VideoFrequency, IAMTVTunerget_VideoFrequency, dshow.iamtvtuner_get_videofrequency, get_VideoFrequency, get_VideoFrequency method [DirectShow], get_VideoFrequency method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_VideoFrequency
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
 - IAMTVTuner::get_VideoFrequency
 - strmif/IAMTVTuner::get_VideoFrequency
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
 - IAMTVTuner.get_VideoFrequency
---

# IAMTVTuner::get_VideoFrequency


## -description

The <code>get_VideoFrequency</code> method retrieves the current video frequency.

## -parameters

### -param lFreq [out]

Pointer to a variable that receives the video frequency, in hertz (Hz).

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This is a diagnostic method that enables you to examine the exact frequency being used for a given channel.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>