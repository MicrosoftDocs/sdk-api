---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_InnerFECRate
title: IBDA_DigitalDemodulator::get_InnerFECRate (bdaiface.h)
description: The get_InnerFECRate method retrieves the inner forward error correction rate being used on the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_InnerFECRate method","IBDA_DigitalDemodulator.get_InnerFECRate","IBDA_DigitalDemodulator::get_InnerFECRate","IBDA_DigitalDemodulatorget_InnerFECRate","bdaiface/IBDA_DigitalDemodulator::get_InnerFECRate","get_InnerFECRate","get_InnerFECRate method [Microsoft TV Technologies]","get_InnerFECRate method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_innerfecrate"]
old-location: mstv\ibda_digitaldemodulator_get_innerfecrate.htm
tech.root: mstv
ms.assetid: 56fb0c34-8c28-4eff-a1dd-d82c31b0e430
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_InnerFECRate method, IBDA_DigitalDemodulator.get_InnerFECRate, IBDA_DigitalDemodulator::get_InnerFECRate, IBDA_DigitalDemodulatorget_InnerFECRate, bdaiface/IBDA_DigitalDemodulator::get_InnerFECRate, get_InnerFECRate, get_InnerFECRate method [Microsoft TV Technologies], get_InnerFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_innerfecrate
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
 - IBDA_DigitalDemodulator::get_InnerFECRate
 - bdaiface/IBDA_DigitalDemodulator::get_InnerFECRate
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
 - IBDA_DigitalDemodulator.get_InnerFECRate
---

# IBDA_DigitalDemodulator::get_InnerFECRate


## -description

The <b>get_InnerFECRate</b> method retrieves the inner forward error correction rate being used on the signal.

## -parameters

### -param pFECRate [out]

Pointer that receives a <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> variable that indicates the rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecrate">IBDA_DigitalDemodulator::get_OuterFECRate</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecrate">IBDA_DigitalDemodulator::put_InnerFECRate</a>