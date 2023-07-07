---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_SymbolRate
title: IBDA_DigitalDemodulator::put_SymbolRate (bdaiface.h)
description: The put_SymbolRate method specifies the symbol rate for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_SymbolRate method","IBDA_DigitalDemodulator.put_SymbolRate","IBDA_DigitalDemodulator::put_SymbolRate","IBDA_DigitalDemodulatorput_SymbolRate","bdaiface/IBDA_DigitalDemodulator::put_SymbolRate","mstv.ibda_digitaldemodulator_put_symbolrate","put_SymbolRate","put_SymbolRate method [Microsoft TV Technologies]","put_SymbolRate method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_symbolrate.htm
tech.root: mstv
ms.assetid: ec37e7a5-d2e8-468a-8b5b-d1a1fa538bfe
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_SymbolRate method, IBDA_DigitalDemodulator.put_SymbolRate, IBDA_DigitalDemodulator::put_SymbolRate, IBDA_DigitalDemodulatorput_SymbolRate, bdaiface/IBDA_DigitalDemodulator::put_SymbolRate, mstv.ibda_digitaldemodulator_put_symbolrate, put_SymbolRate, put_SymbolRate method [Microsoft TV Technologies], put_SymbolRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_SymbolRate
 - bdaiface/IBDA_DigitalDemodulator::put_SymbolRate
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
 - IBDA_DigitalDemodulator.put_SymbolRate
---

# IBDA_DigitalDemodulator::put_SymbolRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SymbolRate</b> method specifies the symbol rate for the signal.

## -parameters

### -param pSymbolRate [in]

Pointer to a ULONG that specifies the symbol rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_symbolrate">IBDA_DigitalDemodulator::get_SymbolRate</a>