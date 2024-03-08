---
UID: NF:segment.IMSVidAnalogTuner.get_VideoFrequency
title: IMSVidAnalogTuner::get_VideoFrequency (segment.h)
description: The get_VideoFrequency method retrieves the tuner's video frequency for testing purposes.
helpviewer_keywords: ["IMSVidAnalogTuner interface [Microsoft TV Technologies]","get_VideoFrequency method","IMSVidAnalogTuner.get_VideoFrequency","IMSVidAnalogTuner::get_VideoFrequency","IMSVidAnalogTunerget_VideoFrequency","get_VideoFrequency","get_VideoFrequency method [Microsoft TV Technologies]","get_VideoFrequency method [Microsoft TV Technologies]","IMSVidAnalogTuner interface","mstv.imsvidanalogtuner_get_videofrequency","segment/IMSVidAnalogTuner::get_VideoFrequency"]
old-location: mstv\imsvidanalogtuner_get_videofrequency.htm
tech.root: mstv
ms.assetid: c6ed5c47-c2cb-4025-9b93-57db25b5cec5
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_VideoFrequency method, IMSVidAnalogTuner.get_VideoFrequency, IMSVidAnalogTuner::get_VideoFrequency, IMSVidAnalogTunerget_VideoFrequency, get_VideoFrequency, get_VideoFrequency method [Microsoft TV Technologies], get_VideoFrequency method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_videofrequency, segment/IMSVidAnalogTuner::get_VideoFrequency
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
 - IMSVidAnalogTuner::get_VideoFrequency
 - segment/IMSVidAnalogTuner::get_VideoFrequency
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
 - IMSVidAnalogTuner.get_VideoFrequency
---

# IMSVidAnalogTuner::get_VideoFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_VideoFrequency</b> method retrieves the tuner's video frequency for testing purposes.

## -parameters

### -param lcc [out]

Pointer to a variable that receives the video frequency, in hertz (Hz).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is intended for diagnostic and testing purposes.

## -see-also

<a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_videofrequency">IAMTVTuner::get_VideoFrequency</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>