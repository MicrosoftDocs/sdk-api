---
UID: NF:tuner.ITuner.get_SignalStrength
title: ITuner::get_SignalStrength (tuner.h)
description: The get_SignalStrength method retrieves the Network Provider-specific signal strength metric.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","get_SignalStrength method","ITuner.get_SignalStrength","ITuner::get_SignalStrength","ITunerget_SignalStrength","get_SignalStrength","get_SignalStrength method [Microsoft TV Technologies]","get_SignalStrength method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_get_signalstrength","tuner/ITuner::get_SignalStrength"]
old-location: mstv\ituner_get_signalstrength.htm
tech.root: mstv
ms.assetid: 3040f56b-2c60-43c8-81b8-5c3538db08db
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_SignalStrength method, ITuner.get_SignalStrength, ITuner::get_SignalStrength, ITunerget_SignalStrength, get_SignalStrength, get_SignalStrength method [Microsoft TV Technologies], get_SignalStrength method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_signalstrength, tuner/ITuner::get_SignalStrength
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
 - ITuner::get_SignalStrength
 - tuner/ITuner::get_SignalStrength
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
 - ITuner.get_SignalStrength
---

# ITuner::get_SignalStrength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalStrength</b> method retrieves the Network Provider-specific signal strength metric.

## -parameters

### -param Strength [out]

Receives the signal strength.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value -1 means can't determine, 0 means not tuned, highest value means best signal. For digital tuners, this also accounts for the FEC bit error rate (BER).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>