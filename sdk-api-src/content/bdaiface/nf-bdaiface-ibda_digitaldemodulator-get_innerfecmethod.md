---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_InnerFECMethod
title: IBDA_DigitalDemodulator::get_InnerFECMethod (bdaiface.h)
description: The get_InnerFECMethod method retrieves the inner forward error correction method.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_InnerFECMethod method","IBDA_DigitalDemodulator.get_InnerFECMethod","IBDA_DigitalDemodulator::get_InnerFECMethod","IBDA_DigitalDemodulatorget_InnerFECMethod","bdaiface/IBDA_DigitalDemodulator::get_InnerFECMethod","get_InnerFECMethod","get_InnerFECMethod method [Microsoft TV Technologies]","get_InnerFECMethod method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_innerfecmethod"]
old-location: mstv\ibda_digitaldemodulator_get_innerfecmethod.htm
tech.root: mstv
ms.assetid: a245c9fa-6f1e-4aa6-a5bf-b9707244a9e2
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_InnerFECMethod method, IBDA_DigitalDemodulator.get_InnerFECMethod, IBDA_DigitalDemodulator::get_InnerFECMethod, IBDA_DigitalDemodulatorget_InnerFECMethod, bdaiface/IBDA_DigitalDemodulator::get_InnerFECMethod, get_InnerFECMethod, get_InnerFECMethod method [Microsoft TV Technologies], get_InnerFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_innerfecmethod
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
 - IBDA_DigitalDemodulator::get_InnerFECMethod
 - bdaiface/IBDA_DigitalDemodulator::get_InnerFECMethod
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
 - IBDA_DigitalDemodulator.get_InnerFECMethod
---

# IBDA_DigitalDemodulator::get_InnerFECMethod


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InnerFECMethod</b> method retrieves the inner forward error correction method.

## -parameters

### -param pFECMethod [out]

Pointer that receives an <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> variable.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecmethod">IBDA_DigitalDemodulator::get_OuterFECMethod</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecmethod">IBDA_DigitalDemodulator::put_InnerFECMethod</a>