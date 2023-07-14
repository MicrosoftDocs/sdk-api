---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_SymbolRate
title: IBDA_DigitalDemodulator::get_SymbolRate (bdaiface.h)
description: The get_SymbolRate method retrieves the symbol rate for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_SymbolRate method","IBDA_DigitalDemodulator.get_SymbolRate","IBDA_DigitalDemodulator::get_SymbolRate","IBDA_DigitalDemodulatorget_SymbolRate","bdaiface/IBDA_DigitalDemodulator::get_SymbolRate","get_SymbolRate","get_SymbolRate method [Microsoft TV Technologies]","get_SymbolRate method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_symbolrate"]
old-location: mstv\ibda_digitaldemodulator_get_symbolrate.htm
tech.root: mstv
ms.assetid: d3640389-2533-4e6f-bc3e-7dceef76866b
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_SymbolRate method, IBDA_DigitalDemodulator.get_SymbolRate, IBDA_DigitalDemodulator::get_SymbolRate, IBDA_DigitalDemodulatorget_SymbolRate, bdaiface/IBDA_DigitalDemodulator::get_SymbolRate, get_SymbolRate, get_SymbolRate method [Microsoft TV Technologies], get_SymbolRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_symbolrate
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
 - IBDA_DigitalDemodulator::get_SymbolRate
 - bdaiface/IBDA_DigitalDemodulator::get_SymbolRate
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
 - IBDA_DigitalDemodulator.get_SymbolRate
---

# IBDA_DigitalDemodulator::get_SymbolRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SymbolRate</b> method retrieves the symbol rate for the signal.

## -parameters

### -param pSymbolRate [out]

Pointer that receives the symbol rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_symbolrate">IBDA_DigitalDemodulator::put_SymbolRate</a>