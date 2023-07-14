---
UID: NF:segment.IMSVidTuner.get_TuningSpace
title: IMSVidTuner::get_TuningSpace (segment.h)
description: The get_TuningSpace method retrieves the current tuning space.
helpviewer_keywords: ["IMSVidTuner interface [Microsoft TV Technologies]","get_TuningSpace method","IMSVidTuner.get_TuningSpace","IMSVidTuner::get_TuningSpace","IMSVidTunerget_TuningSpace","get_TuningSpace","get_TuningSpace method [Microsoft TV Technologies]","get_TuningSpace method [Microsoft TV Technologies]","IMSVidTuner interface","mstv.imsvidtuner_get_tuningspace","segment/IMSVidTuner::get_TuningSpace"]
old-location: mstv\imsvidtuner_get_tuningspace.htm
tech.root: mstv
ms.assetid: d46e7d8a-5111-4737-897b-9e1357e3249a
ms.date: 12/05/2018
ms.keywords: IMSVidTuner interface [Microsoft TV Technologies],get_TuningSpace method, IMSVidTuner.get_TuningSpace, IMSVidTuner::get_TuningSpace, IMSVidTunerget_TuningSpace, get_TuningSpace, get_TuningSpace method [Microsoft TV Technologies], get_TuningSpace method [Microsoft TV Technologies],IMSVidTuner interface, mstv.imsvidtuner_get_tuningspace, segment/IMSVidTuner::get_TuningSpace
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
 - IMSVidTuner::get_TuningSpace
 - segment/IMSVidTuner::get_TuningSpace
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
 - IMSVidTuner.get_TuningSpace
---

# IMSVidTuner::get_TuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TuningSpace</b> method retrieves the current tuning space.

## -parameters

### -param plTS [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The returned <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidtuner-put_tuningspace">IMSVidTuner::put_TuningSpace</a>



<a href="/previous-versions/windows/desktop/mstv/the-microsoft-unified-tuning-model">The Microsoft Unified Tuning Model</a>