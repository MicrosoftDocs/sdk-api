---
UID: NF:tuner.IDVBSTuningSpace.get_HighOscillator
title: IDVBSTuningSpace::get_HighOscillator (tuner.h)
description: The get_HighOscillator method retrieves the high oscillator frequency.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","get_HighOscillator method","IDVBSTuningSpace.get_HighOscillator","IDVBSTuningSpace::get_HighOscillator","IDVBSTuningSpaceget_HighOscillator","get_HighOscillator","get_HighOscillator method [Microsoft TV Technologies]","get_HighOscillator method [Microsoft TV Technologies]","IDVBSTuningSpace interface","mstv.idvbstuningspace_get_highoscillator","tuner/IDVBSTuningSpace::get_HighOscillator"]
old-location: mstv\idvbstuningspace_get_highoscillator.htm
tech.root: mstv
ms.assetid: e3b70684-5066-411e-9946-ccfc1efa3e7c
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_HighOscillator method, IDVBSTuningSpace.get_HighOscillator, IDVBSTuningSpace::get_HighOscillator, IDVBSTuningSpaceget_HighOscillator, get_HighOscillator, get_HighOscillator method [Microsoft TV Technologies], get_HighOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_highoscillator, tuner/IDVBSTuningSpace::get_HighOscillator
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
 - IDVBSTuningSpace::get_HighOscillator
 - tuner/IDVBSTuningSpace::get_HighOscillator
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
 - IDVBSTuningSpace.get_HighOscillator
---

# IDVBSTuningSpace::get_HighOscillator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_HighOscillator</b> method retrieves the high oscillator frequency.

## -parameters

### -param HighOscillator [out]

Receives the high oscillator frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>