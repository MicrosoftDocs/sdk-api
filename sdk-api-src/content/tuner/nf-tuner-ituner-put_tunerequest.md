---
UID: NF:tuner.ITuner.put_TuneRequest
title: ITuner::put_TuneRequest (tuner.h)
description: The put_TuneRequest method sets the tune request currently in effect for the Network Provider.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","put_TuneRequest method","ITuner.put_TuneRequest","ITuner::put_TuneRequest","ITunerput_TuneRequest","mstv.ituner_put_tunerequest","put_TuneRequest","put_TuneRequest method [Microsoft TV Technologies]","put_TuneRequest method [Microsoft TV Technologies]","ITuner interface","tuner/ITuner::put_TuneRequest"]
old-location: mstv\ituner_put_tunerequest.htm
tech.root: mstv
ms.assetid: 69f71855-86d0-4ef9-a168-14e79461ec98
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],put_TuneRequest method, ITuner.put_TuneRequest, ITuner::put_TuneRequest, ITunerput_TuneRequest, mstv.ituner_put_tunerequest, put_TuneRequest, put_TuneRequest method [Microsoft TV Technologies], put_TuneRequest method [Microsoft TV Technologies],ITuner interface, tuner/ITuner::put_TuneRequest
f1_keywords:
- tuner/ITuner.put_TuneRequest
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- ITuner.put_TuneRequest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuner::put_TuneRequest


## -description



The <b>put_TuneRequest</b> method sets the tune request currently in effect for the Network Provider.




## -parameters




### -param TuneRequest [in]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> object that will be used to set the Network Provider.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Calling this method initiates a tuning operation based on the properties of the tune request. The tuning operation may be asynchronously attempted.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>
 

 

