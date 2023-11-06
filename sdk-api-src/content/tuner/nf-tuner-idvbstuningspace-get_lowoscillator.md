---
UID: NF:tuner.IDVBSTuningSpace.get_LowOscillator
title: IDVBSTuningSpace::get_LowOscillator (tuner.h)
description: The get_LowOscillator method retrieves the low oscillator frequency.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","get_LowOscillator method","IDVBSTuningSpace.get_LowOscillator","IDVBSTuningSpace::get_LowOscillator","IDVBSTuningSpaceget_LowOscillator","get_LowOscillator","get_LowOscillator method [Microsoft TV Technologies]","get_LowOscillator method [Microsoft TV Technologies]","IDVBSTuningSpace interface","mstv.idvbstuningspace_get_lowoscillator","tuner/IDVBSTuningSpace::get_LowOscillator"]
old-location: mstv\idvbstuningspace_get_lowoscillator.htm
tech.root: mstv
ms.assetid: 7f48902d-9242-4791-b0f1-fc4ab5bd85c0
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_LowOscillator method, IDVBSTuningSpace.get_LowOscillator, IDVBSTuningSpace::get_LowOscillator, IDVBSTuningSpaceget_LowOscillator, get_LowOscillator, get_LowOscillator method [Microsoft TV Technologies], get_LowOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_lowoscillator, tuner/IDVBSTuningSpace::get_LowOscillator
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
 - IDVBSTuningSpace::get_LowOscillator
 - tuner/IDVBSTuningSpace::get_LowOscillator
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
 - IDVBSTuningSpace.get_LowOscillator
---

# IDVBSTuningSpace::get_LowOscillator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_LowOscillator</b> method retrieves the low oscillator frequency.

## -parameters

### -param LowOscillator [out]

Receives the low oscillator frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>