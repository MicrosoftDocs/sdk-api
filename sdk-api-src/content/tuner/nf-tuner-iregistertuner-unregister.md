---
UID: NF:tuner.IRegisterTuner.Unregister
title: IRegisterTuner::Unregister (tuner.h)
description: This feature is expected to be available on a future version of the Windows operating system.
helpviewer_keywords: ["IRegisterTuner interface [Microsoft TV Technologies]","Unregister method","IRegisterTuner.Unregister","IRegisterTuner::Unregister","IRegisterTunerUnregister","Unregister","Unregister method [Microsoft TV Technologies]","Unregister method [Microsoft TV Technologies]","IRegisterTuner interface","mstv.iregistertuner_unregister","tuner/IRegisterTuner::Unregister"]
old-location: mstv\iregistertuner_unregister.htm
tech.root: mstv
ms.assetid: 4aa616a6-ffaf-4f7e-8eba-eb11f5b55601
ms.date: 12/05/2018
ms.keywords: IRegisterTuner interface [Microsoft TV Technologies],Unregister method, IRegisterTuner.Unregister, IRegisterTuner::Unregister, IRegisterTunerUnregister, Unregister, Unregister method [Microsoft TV Technologies], Unregister method [Microsoft TV Technologies],IRegisterTuner interface, mstv.iregistertuner_unregister, tuner/IRegisterTuner::Unregister
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
 - IRegisterTuner::Unregister
 - tuner/IRegisterTuner::Unregister
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
 - IRegisterTuner.Unregister
---

# IRegisterTuner::Unregister


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This feature is expected to be available on a future version of the Windows operating system.
        



The <b>Unregister</b> method unregisters an apartment-threaded tuner and a tuner marshaller that were registered by <b>IRegisterTuner::Register</b>.



## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iregistertuner">IRegisterTuner Interface</a>
