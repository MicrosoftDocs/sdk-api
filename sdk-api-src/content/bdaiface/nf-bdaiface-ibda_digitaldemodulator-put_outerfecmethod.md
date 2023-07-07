---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_OuterFECMethod
title: IBDA_DigitalDemodulator::put_OuterFECMethod (bdaiface.h)
description: The put_OuterFECMethod method specifies the outer forward error correction method for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_OuterFECMethod method","IBDA_DigitalDemodulator.put_OuterFECMethod","IBDA_DigitalDemodulator::put_OuterFECMethod","IBDA_DigitalDemodulatorput_OuterFECMethod","bdaiface/IBDA_DigitalDemodulator::put_OuterFECMethod","mstv.ibda_digitaldemodulator_put_outerfecmethod","put_OuterFECMethod","put_OuterFECMethod method [Microsoft TV Technologies]","put_OuterFECMethod method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_outerfecmethod.htm
tech.root: mstv
ms.assetid: 8ec9c75b-5f71-4a07-8234-8f38b96b962d
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_OuterFECMethod method, IBDA_DigitalDemodulator.put_OuterFECMethod, IBDA_DigitalDemodulator::put_OuterFECMethod, IBDA_DigitalDemodulatorput_OuterFECMethod, bdaiface/IBDA_DigitalDemodulator::put_OuterFECMethod, mstv.ibda_digitaldemodulator_put_outerfecmethod, put_OuterFECMethod, put_OuterFECMethod method [Microsoft TV Technologies], put_OuterFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_OuterFECMethod
 - bdaiface/IBDA_DigitalDemodulator::put_OuterFECMethod
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
 - IBDA_DigitalDemodulator.put_OuterFECMethod
---

# IBDA_DigitalDemodulator::put_OuterFECMethod


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OuterFECMethod</b> method specifies the outer forward error correction method for the signal.

## -parameters

### -param pFECMethod [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> variable.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecmethod">IBDA_DigitalDemodulator::get_OuterFECMethod</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecmethod">IBDA_DigitalDemodulator::put_InnerFECMethod</a>