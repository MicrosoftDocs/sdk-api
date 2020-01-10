---
UID: NF:segment.IMSVidAnalogTuner.put_CountryCode
title: IMSVidAnalogTuner::put_CountryCode (segment.h)
description: The put_CountryCode method specifies the tuner's country/region code.
old-location: mstv\imsvidanalogtuner_put_countrycode.htm
tech.root: mstv
ms.assetid: e6ec6975-8953-45df-9d86-cf8b8888bba6
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],put_CountryCode method, IMSVidAnalogTuner.put_CountryCode, IMSVidAnalogTuner::put_CountryCode, IMSVidAnalogTunerput_CountryCode, mstv.imsvidanalogtuner_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IMSVidAnalogTuner interface, segment/IMSVidAnalogTuner::put_CountryCode
f1_keywords:
- segment/IMSVidAnalogTuner.put_CountryCode
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidAnalogTuner.put_CountryCode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidAnalogTuner::put_CountryCode


## -description


The <b>put_CountryCode</b> method specifies the tuner's country/region code.


## -parameters




### -param lcc [in]

Specifies the international country/region code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Do not confuse the international country/region code with the LCID. The country/region code establishes the mapping between channel numbers and frequencies.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_countrycode">IAMTuner::put_CountryCode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidanalogtuner-get_countrycode">IMSVidAnalogTuner::get_CountryCode</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>
 

 

