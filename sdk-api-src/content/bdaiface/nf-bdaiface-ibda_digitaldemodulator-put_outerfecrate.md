---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_OuterFECRate
title: IBDA_DigitalDemodulator::put_OuterFECRate (bdaiface.h)
description: The put_OuterFECRate method specifies the outer forward error correction rate for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_OuterFECRate method","IBDA_DigitalDemodulator.put_OuterFECRate","IBDA_DigitalDemodulator::put_OuterFECRate","IBDA_DigitalDemodulatorput_OuterFECRate","bdaiface/IBDA_DigitalDemodulator::put_OuterFECRate","mstv.ibda_digitaldemodulator_put_outerfecrate","put_OuterFECRate","put_OuterFECRate method [Microsoft TV Technologies]","put_OuterFECRate method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_outerfecrate.htm
tech.root: mstv
ms.assetid: 60c35bd1-b971-411b-92bf-bbed41fc984c
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_OuterFECRate method, IBDA_DigitalDemodulator.put_OuterFECRate, IBDA_DigitalDemodulator::put_OuterFECRate, IBDA_DigitalDemodulatorput_OuterFECRate, bdaiface/IBDA_DigitalDemodulator::put_OuterFECRate, mstv.ibda_digitaldemodulator_put_outerfecrate, put_OuterFECRate, put_OuterFECRate method [Microsoft TV Technologies], put_OuterFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_OuterFECRate
 - bdaiface/IBDA_DigitalDemodulator::put_OuterFECRate
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
 - IBDA_DigitalDemodulator.put_OuterFECRate
---

# IBDA_DigitalDemodulator::put_OuterFECRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OuterFECRate</b> method specifies the outer forward error correction rate for the signal.

## -parameters

### -param pFECRate [in]

Pointer to a <a href="/previous-versions/windows/desktop/mstv/binaryconvolutioncoderate">BinaryConvolutionCodeRate</a> variable that specifies the FEC rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecrate">IBDA_DigitalDemodulator::get_OuterFECRate</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecrate">IBDA_DigitalDemodulator::put_InnerFECRate</a>