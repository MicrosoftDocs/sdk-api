---
UID: NF:tuner.ITuner.get_TuningSpace
title: ITuner::get_TuningSpace (tuner.h)
description: The get_TuningSpace method gets the tuning space currently in effect for the Network Provider.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","get_TuningSpace method","ITuner.get_TuningSpace","ITuner::get_TuningSpace","ITunerget_TuningSpace","get_TuningSpace","get_TuningSpace method [Microsoft TV Technologies]","get_TuningSpace method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_get_tuningspace","tuner/ITuner::get_TuningSpace"]
old-location: mstv\ituner_get_tuningspace.htm
tech.root: mstv
ms.assetid: 01b6a280-d489-4b4f-ae87-17c9b9bb2838
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_TuningSpace method, ITuner.get_TuningSpace, ITuner::get_TuningSpace, ITunerget_TuningSpace, get_TuningSpace, get_TuningSpace method [Microsoft TV Technologies], get_TuningSpace method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_tuningspace, tuner/ITuner::get_TuningSpace
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
 - ITuner::get_TuningSpace
 - tuner/ITuner::get_TuningSpace
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
 - ITuner.get_TuningSpace
---

# ITuner::get_TuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TuningSpace</b> method gets the tuning space currently in effect for the Network Provider.

## -parameters

### -param TuningSpace [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface pointer that will be set to the current tuning space.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>