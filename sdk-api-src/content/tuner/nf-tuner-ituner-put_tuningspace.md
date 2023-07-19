---
UID: NF:tuner.ITuner.put_TuningSpace
title: ITuner::put_TuningSpace (tuner.h)
description: The put_TuningSpace method sets the tuning space for the Network Provider.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","put_TuningSpace method","ITuner.put_TuningSpace","ITuner::put_TuningSpace","ITunerput_TuningSpace","mstv.ituner_put_tuningspace","put_TuningSpace","put_TuningSpace method [Microsoft TV Technologies]","put_TuningSpace method [Microsoft TV Technologies]","ITuner interface","tuner/ITuner::put_TuningSpace"]
old-location: mstv\ituner_put_tuningspace.htm
tech.root: mstv
ms.assetid: ae764317-3441-4abb-90e8-f7720cdfd957
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],put_TuningSpace method, ITuner.put_TuningSpace, ITuner::put_TuningSpace, ITunerput_TuningSpace, mstv.ituner_put_tuningspace, put_TuningSpace, put_TuningSpace method [Microsoft TV Technologies], put_TuningSpace method [Microsoft TV Technologies],ITuner interface, tuner/ITuner::put_TuningSpace
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - ITuner::put_TuningSpace
 - tuner/ITuner::put_TuningSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuner.put_TuningSpace
---

# ITuner::put_TuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TuningSpace</b> method sets the tuning space for the Network Provider.

## -parameters

### -param TuningSpace [in]

Pointer to the tuning space that will be set in the Network Provider.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>