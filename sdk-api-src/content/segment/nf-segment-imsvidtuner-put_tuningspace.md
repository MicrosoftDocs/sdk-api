---
UID: NF:segment.IMSVidTuner.put_TuningSpace
title: IMSVidTuner::put_TuningSpace (segment.h)
description: The put_TuningSpace method specifies the tuning space.
helpviewer_keywords: ["IMSVidTuner interface [Microsoft TV Technologies]","put_TuningSpace method","IMSVidTuner.put_TuningSpace","IMSVidTuner::put_TuningSpace","IMSVidTunerput_TuningSpace","mstv.imsvidtuner_put_tuningspace","put_TuningSpace","put_TuningSpace method [Microsoft TV Technologies]","put_TuningSpace method [Microsoft TV Technologies]","IMSVidTuner interface","segment/IMSVidTuner::put_TuningSpace"]
old-location: mstv\imsvidtuner_put_tuningspace.htm
tech.root: mstv
ms.assetid: b1da0078-0c5e-439e-9419-670e9e0f812c
ms.date: 12/05/2018
ms.keywords: IMSVidTuner interface [Microsoft TV Technologies],put_TuningSpace method, IMSVidTuner.put_TuningSpace, IMSVidTuner::put_TuningSpace, IMSVidTunerput_TuningSpace, mstv.imsvidtuner_put_tuningspace, put_TuningSpace, put_TuningSpace method [Microsoft TV Technologies], put_TuningSpace method [Microsoft TV Technologies],IMSVidTuner interface, segment/IMSVidTuner::put_TuningSpace
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
 - IMSVidTuner::put_TuningSpace
 - segment/IMSVidTuner::put_TuningSpace
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
 - IMSVidTuner.put_TuningSpace
---

# IMSVidTuner::put_TuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TuningSpace</b> method specifies the tuning space.

## -parameters

### -param plTS [in]

Specifies a pointer to the tuning space's <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidtuner-get_tuningspace">IMSVidTuner::get_TuningSpace</a>



<a href="/previous-versions/windows/desktop/mstv/the-microsoft-unified-tuning-model">The Microsoft Unified Tuning Model</a>