---
UID: NF:segment.IMSVidTuner.put_Tune
title: IMSVidTuner::put_Tune (segment.h)
description: The put_Tune method specifies the tune request.
helpviewer_keywords: ["IMSVidTuner interface [Microsoft TV Technologies]","put_Tune method","IMSVidTuner.put_Tune","IMSVidTuner::put_Tune","IMSVidTunerput_Tune","mstv.imsvidtuner_put_tune","put_Tune","put_Tune method [Microsoft TV Technologies]","put_Tune method [Microsoft TV Technologies]","IMSVidTuner interface","segment/IMSVidTuner::put_Tune"]
old-location: mstv\imsvidtuner_put_tune.htm
tech.root: mstv
ms.assetid: 31139b6f-aad9-495b-9e8c-39026c8e81a9
ms.date: 12/05/2018
ms.keywords: IMSVidTuner interface [Microsoft TV Technologies],put_Tune method, IMSVidTuner.put_Tune, IMSVidTuner::put_Tune, IMSVidTunerput_Tune, mstv.imsvidtuner_put_tune, put_Tune, put_Tune method [Microsoft TV Technologies], put_Tune method [Microsoft TV Technologies],IMSVidTuner interface, segment/IMSVidTuner::put_Tune
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
 - IMSVidTuner::put_Tune
 - segment/IMSVidTuner::put_Tune
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
 - IMSVidTuner.put_Tune
---

# IMSVidTuner::put_Tune


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">put_Tune</a> method specifies the tune request.

## -parameters

### -param pTR [in]

Specifies a pointer to the tune request's <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidtuner-get_tune">IMSVidTuner::get_Tune</a>



<a href="/previous-versions/windows/desktop/mstv/the-microsoft-unified-tuning-model">The Microsoft Unified Tuning Model</a>