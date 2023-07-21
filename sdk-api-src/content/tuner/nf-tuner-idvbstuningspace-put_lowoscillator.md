---
UID: NF:tuner.IDVBSTuningSpace.put_LowOscillator
title: IDVBSTuningSpace::put_LowOscillator (tuner.h)
description: The put_LowOscillator method sets the low oscillator frequency.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","put_LowOscillator method","IDVBSTuningSpace.put_LowOscillator","IDVBSTuningSpace::put_LowOscillator","IDVBSTuningSpaceput_LowOscillator","mstv.idvbstuningspace_put_lowoscillator","put_LowOscillator","put_LowOscillator method [Microsoft TV Technologies]","put_LowOscillator method [Microsoft TV Technologies]","IDVBSTuningSpace interface","tuner/IDVBSTuningSpace::put_LowOscillator"]
old-location: mstv\idvbstuningspace_put_lowoscillator.htm
tech.root: mstv
ms.assetid: cadc2818-d54c-410a-9894-28baa51b9b01
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],put_LowOscillator method, IDVBSTuningSpace.put_LowOscillator, IDVBSTuningSpace::put_LowOscillator, IDVBSTuningSpaceput_LowOscillator, mstv.idvbstuningspace_put_lowoscillator, put_LowOscillator, put_LowOscillator method [Microsoft TV Technologies], put_LowOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, tuner/IDVBSTuningSpace::put_LowOscillator
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
 - IDVBSTuningSpace::put_LowOscillator
 - tuner/IDVBSTuningSpace::put_LowOscillator
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
 - IDVBSTuningSpace.put_LowOscillator
---

# IDVBSTuningSpace::put_LowOscillator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_LowOscillator</b> method sets the low oscillator frequency.

## -parameters

### -param LowOscillator [in]

Specifies the low oscillator frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>