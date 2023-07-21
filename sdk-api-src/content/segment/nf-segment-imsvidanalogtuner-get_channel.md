---
UID: NF:segment.IMSVidAnalogTuner.get_Channel
title: IMSVidAnalogTuner::get_Channel (segment.h)
description: The get_Channel method retrieves the tuner's current channel.
helpviewer_keywords: ["IMSVidAnalogTuner interface [Microsoft TV Technologies]","get_Channel method","IMSVidAnalogTuner.get_Channel","IMSVidAnalogTuner::get_Channel","IMSVidAnalogTunerget_Channel","get_Channel","get_Channel method [Microsoft TV Technologies]","get_Channel method [Microsoft TV Technologies]","IMSVidAnalogTuner interface","mstv.imsvidanalogtuner_get_channel","segment/IMSVidAnalogTuner::get_Channel"]
old-location: mstv\imsvidanalogtuner_get_channel.htm
tech.root: mstv
ms.assetid: 9d62cd70-02cf-4454-b5b7-da2d623ec95d
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner interface [Microsoft TV Technologies],get_Channel method, IMSVidAnalogTuner.get_Channel, IMSVidAnalogTuner::get_Channel, IMSVidAnalogTunerget_Channel, get_Channel, get_Channel method [Microsoft TV Technologies], get_Channel method [Microsoft TV Technologies],IMSVidAnalogTuner interface, mstv.imsvidanalogtuner_get_channel, segment/IMSVidAnalogTuner::get_Channel
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
 - IMSVidAnalogTuner::get_Channel
 - segment/IMSVidAnalogTuner::get_Channel
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
 - IMSVidAnalogTuner.get_Channel
---

# IMSVidAnalogTuner::get_Channel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Channel</b> method retrieves the tuner's current channel.

## -parameters

### -param Channel [out]

Pointer to a variable that receives the channel.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-get_channel">IAMTuner::get_Channel</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidanalogtuner-put_channel">IMSVidAnalogTuner::put_Channel</a>