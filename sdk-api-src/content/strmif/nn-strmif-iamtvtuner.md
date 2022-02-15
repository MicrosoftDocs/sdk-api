---
UID: NN:strmif.IAMTVTuner
title: IAMTVTuner (strmif.h)
description: The IAMTVTuner interface controls a TV tuner.
helpviewer_keywords: ["IAMTVTuner","IAMTVTuner interface [DirectShow]","IAMTVTuner interface [DirectShow]","described","IAMTVTunerInterface","dshow.iamtvtuner","strmif/IAMTVTuner"]
old-location: dshow\iamtvtuner.htm
tech.root: dshow
ms.assetid: 1c8300c2-be13-4e4c-aa0c-53ce57bc9152
ms.date: 12/05/2018
ms.keywords: IAMTVTuner, IAMTVTuner interface [DirectShow], IAMTVTuner interface [DirectShow],described, IAMTVTunerInterface, dshow.iamtvtuner, strmif/IAMTVTuner
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
 - IAMTVTuner
 - strmif/IAMTVTuner
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
 - IAMTVTuner
---

# IAMTVTuner interface


## -description

The <code>IAMTVTuner</code> interface controls a TV tuner. The <a href="/windows/desktop/DirectShow/tv-tuner-filter">TV Tuner</a> filter implements this interface. Applications can use this interface to set TV channels and to get or set information about their frequencies, and to determine what analog video standards your TV tuner card supports.

The interface supports tuners for analog broadcast television and AM/FM radio. It supports tuners with multiple input pins, to enable multiple devices and multiple transmission types. The TV Tuner filter supports worldwide tuning coverage. It maps TV channels to specific frequencies through the <a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-put_channel">IAMTuner::put_Channel</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-autotune">IAMTVTuner::AutoTune</a> methods. These methods handle the details of the conversion, so that the hardware driver receives an exact frequency.

## -inheritance

The <b>IAMTVTuner</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner</a>. <b>IAMTVTuner</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/analog-television">Analog Television</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner</a>
