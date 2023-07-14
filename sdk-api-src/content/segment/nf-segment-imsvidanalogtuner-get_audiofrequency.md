---
UID: NF:segment.IMSVidAnalogTuner.get_AudioFrequency
title: IMSVidAnalogTuner::get_AudioFrequency (segment.h)
description: The get_AudioFrequency method retrieves the tuner's audio frequency.
helpviewer_keywords: ["IMSVidAnalogTuner interface [Microsoft TV Technologies]","get_AudioFrequency method","IMSVidAnalogTuner.get_AudioFrequency","IMSVidAnalogTuner::get_AudioFrequency","IMSVidAnalogTunerget_AudioFrequency","get_AudioFrequency","get_AudioFrequency method [Microsoft TV Technologies]","get_AudioFrequency method [Microsoft TV Technologies]","IMSVidAnalogTuner interface","mstv.imsvidanalogtuner_get_audiofrequency","segment/IMSVidAnalogTuner::get_AudioFrequency"]
old-location: mstv\imsvidanalogtuner_get_audiofrequency.htm
tech.root: mstv
ms.assetid: d0513ea0-305b-40ac-95ad-ed47a0417046
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_AudioFrequency method, IMSVidAnalogTuner.get_AudioFrequency, IMSVidAnalogTuner::get_AudioFrequency, IMSVidAnalogTunerget_AudioFrequency, get_AudioFrequency, get_AudioFrequency method [Microsoft TV Technologies], get_AudioFrequency method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_audiofrequency, segment/IMSVidAnalogTuner::get_AudioFrequency
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAnalogTuner::get_AudioFrequency
 - segment/IMSVidAnalogTuner::get_AudioFrequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAnalogTuner.get_AudioFrequency
---

# IMSVidAnalogTuner::get_AudioFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AudioFrequency</b> method retrieves the tuner's audio frequency.

## -parameters

### -param lcc [out]

Pointer to a variable that receives the audio frequency, in hertz (Hz).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is intended for diagnostic and testing purposes.

## -see-also

<a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_audiofrequency">IAMTVTuner::get_AudioFrequency</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>