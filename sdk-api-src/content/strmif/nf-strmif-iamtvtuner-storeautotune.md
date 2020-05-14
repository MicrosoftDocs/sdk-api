---
UID: NF:strmif.IAMTVTuner.StoreAutoTune
title: IAMTVTuner::StoreAutoTune (strmif.h)
description: The StoreAutoTune method saves the fine-tuning information for all channels.helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","StoreAutoTune method","IAMTVTuner.StoreAutoTune","IAMTVTuner::StoreAutoTune","IAMTVTunerStoreAutoTune","StoreAutoTune","StoreAutoTune method [DirectShow]","StoreAutoTune method [DirectShow]","IAMTVTuner interface","dshow.iamtvtuner_storeautotune","strmif/IAMTVTuner::StoreAutoTune"]
old-location: dshow\iamtvtuner_storeautotune.htm
tech.root: DirectShow
ms.assetid: 6e39d757-d8bd-4011-9a67-6bf57b5d820b
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],StoreAutoTune method, IAMTVTuner.StoreAutoTune, IAMTVTuner::StoreAutoTune, IAMTVTunerStoreAutoTune, StoreAutoTune, StoreAutoTune method [DirectShow], StoreAutoTune method [DirectShow],IAMTVTuner interface, dshow.iamtvtuner_storeautotune, strmif/IAMTVTuner::StoreAutoTune
f1_keywords:
- strmif/IAMTVTuner.StoreAutoTune
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVTuner::StoreAutoTune


## -description



The <code>StoreAutoTune</code> method saves the fine-tuning information for all channels.




## -parameters






## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Override the channel-to-frequency information stored by this method by setting a new country/region code in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_countrycode">IAMTuner::put_CountryCode</a> method. For a listing of country/region codes, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

