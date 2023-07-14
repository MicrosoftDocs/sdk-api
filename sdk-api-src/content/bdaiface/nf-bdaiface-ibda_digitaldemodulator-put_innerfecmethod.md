---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_InnerFECMethod
title: IBDA_DigitalDemodulator::put_InnerFECMethod (bdaiface.h)
description: The put_InnerFECMethod method specifies the inner forward error correction method for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_InnerFECMethod method","IBDA_DigitalDemodulator.put_InnerFECMethod","IBDA_DigitalDemodulator::put_InnerFECMethod","IBDA_DigitalDemodulatorput_InnerFECMethod","bdaiface/IBDA_DigitalDemodulator::put_InnerFECMethod","mstv.ibda_digitaldemodulator_put_innerfecmethod","put_InnerFECMethod","put_InnerFECMethod method [Microsoft TV Technologies]","put_InnerFECMethod method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_innerfecmethod.htm
tech.root: mstv
ms.assetid: 618074c0-5139-4373-8bcd-9a8fd90a4ed7
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_InnerFECMethod method, IBDA_DigitalDemodulator.put_InnerFECMethod, IBDA_DigitalDemodulator::put_InnerFECMethod, IBDA_DigitalDemodulatorput_InnerFECMethod, bdaiface/IBDA_DigitalDemodulator::put_InnerFECMethod, mstv.ibda_digitaldemodulator_put_innerfecmethod, put_InnerFECMethod, put_InnerFECMethod method [Microsoft TV Technologies], put_InnerFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_InnerFECMethod
 - bdaiface/IBDA_DigitalDemodulator::put_InnerFECMethod
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
 - IBDA_DigitalDemodulator.put_InnerFECMethod
---

# IBDA_DigitalDemodulator::put_InnerFECMethod


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InnerFECMethod</b> method specifies the inner forward error correction method for the signal.

## -parameters

### -param pFECMethod [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/fecmethod">FECMethod</a> variable that specifies the inner forward error correction method.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_innerfecmethod">IBDA_DigitalDemodulator::get_InnerFECMethod</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_outerfecmethod">IBDA_DigitalDemodulator::put_OuterFECMethod</a>