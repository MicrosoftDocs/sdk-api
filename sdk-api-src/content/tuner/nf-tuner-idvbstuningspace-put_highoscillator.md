---
UID: NF:tuner.IDVBSTuningSpace.put_HighOscillator
title: IDVBSTuningSpace::put_HighOscillator (tuner.h)
description: The put_HighOscillator method sets the high oscillator frequency.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","put_HighOscillator method","IDVBSTuningSpace.put_HighOscillator","IDVBSTuningSpace::put_HighOscillator","IDVBSTuningSpaceput_HighOscillator","mstv.idvbstuningspace_put_highoscillator","put_HighOscillator","put_HighOscillator method [Microsoft TV Technologies]","put_HighOscillator method [Microsoft TV Technologies]","IDVBSTuningSpace interface","tuner/IDVBSTuningSpace::put_HighOscillator"]
old-location: mstv\idvbstuningspace_put_highoscillator.htm
tech.root: mstv
ms.assetid: 0f71008b-dbb6-485b-b196-7c2d215b3064
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],put_HighOscillator method, IDVBSTuningSpace.put_HighOscillator, IDVBSTuningSpace::put_HighOscillator, IDVBSTuningSpaceput_HighOscillator, mstv.idvbstuningspace_put_highoscillator, put_HighOscillator, put_HighOscillator method [Microsoft TV Technologies], put_HighOscillator method [Microsoft TV Technologies],IDVBSTuningSpace interface, tuner/IDVBSTuningSpace::put_HighOscillator
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
 - IDVBSTuningSpace::put_HighOscillator
 - tuner/IDVBSTuningSpace::put_HighOscillator
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
 - IDVBSTuningSpace.put_HighOscillator
---

# IDVBSTuningSpace::put_HighOscillator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_HighOscillator</b> method sets the high oscillator frequency.

## -parameters

### -param HighOscillator [in]

Specifies the high oscillator frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>