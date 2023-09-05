---
UID: NF:tuner.ITuner.Validate
title: ITuner::Validate (tuner.h)
description: The Validate method returns a value indicating that the tune request can be carried out.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","Validate method","ITuner.Validate","ITuner::Validate","ITunerValidate","Validate","Validate method [Microsoft TV Technologies]","Validate method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_validate","tuner/ITuner::Validate"]
old-location: mstv\ituner_validate.htm
tech.root: mstv
ms.assetid: 10b238b1-1c71-4104-8c2d-f8446f0a3466
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],Validate method, ITuner.Validate, ITuner::Validate, ITunerValidate, Validate, Validate method [Microsoft TV Technologies], Validate method [Microsoft TV Technologies],ITuner interface, mstv.ituner_validate, tuner/ITuner::Validate
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
 - ITuner::Validate
 - tuner/ITuner::Validate
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
 - ITuner.Validate
---

# ITuner::Validate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Validate</b> method returns a value indicating that the tune request can be carried out.

## -parameters

### -param TuneRequest [in]

Pointer to the tune request object.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Network Provider will first query for its preferred tune request interface(s). If any are found, the Network Provider will validate that the tune request could be carried out. If none are available, it will then query for its preferred tuning space interface(s). If any are found, the Network Provider will validate that it could configure itself for the given tuning space.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>