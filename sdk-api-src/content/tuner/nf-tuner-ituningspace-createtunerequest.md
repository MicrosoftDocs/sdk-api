---
UID: NF:tuner.ITuningSpace.CreateTuneRequest
title: ITuningSpace::CreateTuneRequest (tuner.h)
description: The CreateTuneRequest method creates an empty (uninitialized) tune request.
helpviewer_keywords: ["CreateTuneRequest","CreateTuneRequest method [Microsoft TV Technologies]","CreateTuneRequest method [Microsoft TV Technologies]","ITuningSpace interface","ITuningSpace interface [Microsoft TV Technologies]","CreateTuneRequest method","ITuningSpace.CreateTuneRequest","ITuningSpace::CreateTuneRequest","ITuningSpaceCreateTuneRequest","mstv.ituningspace_createtunerequest","tuner/ITuningSpace::CreateTuneRequest"]
old-location: mstv\ituningspace_createtunerequest.htm
tech.root: mstv
ms.assetid: 513d4d3e-47df-4a12-80ce-9fc1400af176
ms.date: 12/05/2018
ms.keywords: CreateTuneRequest, CreateTuneRequest method [Microsoft TV Technologies], CreateTuneRequest method [Microsoft TV Technologies],ITuningSpace interface, ITuningSpace interface [Microsoft TV Technologies],CreateTuneRequest method, ITuningSpace.CreateTuneRequest, ITuningSpace::CreateTuneRequest, ITuningSpaceCreateTuneRequest, mstv.ituningspace_createtunerequest, tuner/ITuningSpace::CreateTuneRequest
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - ITuningSpace::CreateTuneRequest
 - tuner/ITuningSpace::CreateTuneRequest
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
 - ITuningSpace.CreateTuneRequest
---

# ITuningSpace::CreateTuneRequest


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>CreateTuneRequest</b> method creates an empty (uninitialized) tune request.

## -parameters

### -param TuneRequest [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface of the new tune request object. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

You can query the returned <b>ITuneRequest</b> pointer for derived interfaces. For more information, see the reference pages for the individual tuning space objects, which are listed in the topic <a href="/previous-versions/windows/desktop/mstv/tuning-model-objects">Tuning Model Objects</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>