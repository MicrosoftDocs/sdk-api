---
UID: NF:tuner.IRegisterTuner.Register
title: IRegisterTuner::Register (tuner.h)
description: This feature is expected to be available on a future version of the Windows operating system.
helpviewer_keywords: ["IRegisterTuner interface [Microsoft TV Technologies]","Register method","IRegisterTuner.Register","IRegisterTuner::Register","IRegisterTunerRegister","Register","Register method [Microsoft TV Technologies]","Register method [Microsoft TV Technologies]","IRegisterTuner interface","mstv.iregistertuner_register","tuner/IRegisterTuner::Register"]
old-location: mstv\iregistertuner_register.htm
tech.root: mstv
ms.assetid: 17a59666-1915-496f-9474-ddd6b3da58f5
ms.date: 12/05/2018
ms.keywords: IRegisterTuner interface [Microsoft TV Technologies],Register method, IRegisterTuner.Register, IRegisterTuner::Register, IRegisterTunerRegister, Register, Register method [Microsoft TV Technologies], Register method [Microsoft TV Technologies],IRegisterTuner interface, mstv.iregistertuner_register, tuner/IRegisterTuner::Register
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
 - IRegisterTuner::Register
 - tuner/IRegisterTuner::Register
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
 - IRegisterTuner.Register
---

# IRegisterTuner::Register


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This feature is expected to be available on a future version of the Windows operating system.
        



The <b>Register</b> method registers an apartment-threaded tuner with the tuner marshaller and registers the tuner marshaller with the graph service provider.

## -parameters

### -param pTuner [in]

Pointer to a variable that specifies the tuner.

### -param pGraph [in]

Pointer to a variable that specifies the graph filter provider.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iregistertuner">IRegisterTuner Interface</a>