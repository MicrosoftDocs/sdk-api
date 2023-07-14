---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_OuterFECRate
title: IBDA_DigitalDemodulator::get_OuterFECRate (bdaiface.h)
description: The get_OuterFECRate method retrieves the outer forward error correction rate for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_OuterFECRate method","IBDA_DigitalDemodulator.get_OuterFECRate","IBDA_DigitalDemodulator::get_OuterFECRate","IBDA_DigitalDemodulatorget_OuterFECRate","bdaiface/IBDA_DigitalDemodulator::get_OuterFECRate","get_OuterFECRate","get_OuterFECRate method [Microsoft TV Technologies]","get_OuterFECRate method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_outerfecrate"]
old-location: mstv\ibda_digitaldemodulator_get_outerfecrate.htm
tech.root: mstv
ms.assetid: 99f6e920-0b2d-4509-9a68-c6404d676b8a
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_OuterFECRate method, IBDA_DigitalDemodulator.get_OuterFECRate, IBDA_DigitalDemodulator::get_OuterFECRate, IBDA_DigitalDemodulatorget_OuterFECRate, bdaiface/IBDA_DigitalDemodulator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_outerfecrate
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IBDA_DigitalDemodulator::get_OuterFECRate
 - bdaiface/IBDA_DigitalDemodulator::get_OuterFECRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DigitalDemodulator.get_OuterFECRate
---

# IBDA_DigitalDemodulator::get_OuterFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OuterFECRate</b> method retrieves the outer forward error correction rate for the signal.

## -parameters

### -param pFECRate [out]

Pointer that receives a <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> variable that indicates the rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_innerfecrate">IBDA_DigitalDemodulator::get_InnerFECRate</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_outerfecrate">IBDA_DigitalDemodulator::put_OuterFECRate</a>