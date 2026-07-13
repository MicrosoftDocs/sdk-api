---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_OuterFECMethod
title: IBDA_DigitalDemodulator::get_OuterFECMethod (bdaiface.h)
description: The get_OuterFECMethod method retrieves the outer forward error correction method for the signal .
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_OuterFECMethod method","IBDA_DigitalDemodulator.get_OuterFECMethod","IBDA_DigitalDemodulator::get_OuterFECMethod","IBDA_DigitalDemodulatorget_OuterFECMethod","bdaiface/IBDA_DigitalDemodulator::get_OuterFECMethod","get_OuterFECMethod","get_OuterFECMethod method [Microsoft TV Technologies]","get_OuterFECMethod method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_outerfecmethod"]
old-location: mstv\ibda_digitaldemodulator_get_outerfecmethod.htm
tech.root: mstv
ms.assetid: 6fbedcba-4b76-4cf0-8fa1-c71140d49643
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_OuterFECMethod method, IBDA_DigitalDemodulator.get_OuterFECMethod, IBDA_DigitalDemodulator::get_OuterFECMethod, IBDA_DigitalDemodulatorget_OuterFECMethod, bdaiface/IBDA_DigitalDemodulator::get_OuterFECMethod, get_OuterFECMethod, get_OuterFECMethod method [Microsoft TV Technologies], get_OuterFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_outerfecmethod
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
 - IBDA_DigitalDemodulator::get_OuterFECMethod
 - bdaiface/IBDA_DigitalDemodulator::get_OuterFECMethod
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
 - IBDA_DigitalDemodulator.get_OuterFECMethod
---

# IBDA_DigitalDemodulator::get_OuterFECMethod


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OuterFECMethod</b> method retrieves the outer forward error correction method for the signal .

## -parameters

### -param pFECMethod [out]

Pointer that receives an <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> variable that indicates the FEC method.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_innerfecmethod">IBDA_DigitalDemodulator::get_InnerFECMethod</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_outerfecmethod">IBDA_DigitalDemodulator::put_OuterFECMethod</a>