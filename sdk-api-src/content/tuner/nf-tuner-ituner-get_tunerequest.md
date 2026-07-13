---
UID: NF:tuner.ITuner.get_TuneRequest
title: ITuner::get_TuneRequest (tuner.h)
description: The get_TuneRequest method gets the tune request currently in effect for the Network Provider.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","get_TuneRequest method","ITuner.get_TuneRequest","ITuner::get_TuneRequest","ITunerget_TuneRequest","get_TuneRequest","get_TuneRequest method [Microsoft TV Technologies]","get_TuneRequest method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_get_tunerequest","tuner/ITuner::get_TuneRequest"]
old-location: mstv\ituner_get_tunerequest.htm
tech.root: mstv
ms.assetid: 45967073-2e09-4490-967f-4ed3c9ed1d7e
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_TuneRequest method, ITuner.get_TuneRequest, ITuner::get_TuneRequest, ITunerget_TuneRequest, get_TuneRequest, get_TuneRequest method [Microsoft TV Technologies], get_TuneRequest method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_tunerequest, tuner/ITuner::get_TuneRequest
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
 - ITuner::get_TuneRequest
 - tuner/ITuner::get_TuneRequest
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
 - ITuner.get_TuneRequest
---

# ITuner::get_TuneRequest


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TuneRequest</b> method gets the tune request currently in effect for the Network Provider.

## -parameters

### -param TuneRequest [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface pointer that will be set to the returned object.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After a tune request is submitted to the Tuner, its Components collection will be filled in. By calling <b>get_TuneRequest</b> after tuning to the program, an application can determine which components are currently available for that program, and then use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_status">IComponent::put_Status</a> method on the Component objects in the collection to activate or inactivate them. This is how an application, for example, changes from an English audio stream to a Spanish audio stream.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>