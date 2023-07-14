---
UID: NF:segment.IMSVidTuner.get_Tune
title: IMSVidTuner::get_Tune (segment.h)
description: The get_Tune method retrieves the current tune request.
helpviewer_keywords: ["IMSVidTuner interface [Microsoft TV Technologies]","get_Tune method","IMSVidTuner.get_Tune","IMSVidTuner::get_Tune","IMSVidTunerget_Tune","get_Tune","get_Tune method [Microsoft TV Technologies]","get_Tune method [Microsoft TV Technologies]","IMSVidTuner interface","mstv.imsvidtuner_get_tune","segment/IMSVidTuner::get_Tune"]
old-location: mstv\imsvidtuner_get_tune.htm
tech.root: mstv
ms.assetid: 189c878d-bf14-4464-96ce-5d2e09118dc4
ms.date: 12/05/2018
ms.keywords: IMSVidTuner interface [Microsoft TV Technologies],get_Tune method, IMSVidTuner.get_Tune, IMSVidTuner::get_Tune, IMSVidTunerget_Tune, get_Tune, get_Tune method [Microsoft TV Technologies], get_Tune method [Microsoft TV Technologies],IMSVidTuner interface, mstv.imsvidtuner_get_tune, segment/IMSVidTuner::get_Tune
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
 - IMSVidTuner::get_Tune
 - segment/IMSVidTuner::get_Tune
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
 - IMSVidTuner.get_Tune
---

# IMSVidTuner::get_Tune


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Tune</b> method retrieves the current tune request.

## -parameters

### -param ppTR [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The returned <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidtuner-put_tune">IMSVidTuner::put_Tune</a>



<a href="/previous-versions/windows/desktop/mstv/the-microsoft-unified-tuning-model">The Microsoft Unified Tuning Model</a>