---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_ModulationType
title: IBDA_DigitalDemodulator::get_ModulationType (bdaiface.h)
description: The get_ModulationType method retrieves the modulation type for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_ModulationType method","IBDA_DigitalDemodulator.get_ModulationType","IBDA_DigitalDemodulator::get_ModulationType","IBDA_DigitalDemodulatorget_ModulationType","bdaiface/IBDA_DigitalDemodulator::get_ModulationType","get_ModulationType","get_ModulationType method [Microsoft TV Technologies]","get_ModulationType method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_modulationtype"]
old-location: mstv\ibda_digitaldemodulator_get_modulationtype.htm
tech.root: mstv
ms.assetid: 0f00553f-c0b1-4ff5-9c92-fe3a1990ef20
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_ModulationType method, IBDA_DigitalDemodulator.get_ModulationType, IBDA_DigitalDemodulator::get_ModulationType, IBDA_DigitalDemodulatorget_ModulationType, bdaiface/IBDA_DigitalDemodulator::get_ModulationType, get_ModulationType, get_ModulationType method [Microsoft TV Technologies], get_ModulationType method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_modulationtype
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
 - IBDA_DigitalDemodulator::get_ModulationType
 - bdaiface/IBDA_DigitalDemodulator::get_ModulationType
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
 - IBDA_DigitalDemodulator.get_ModulationType
---

# IBDA_DigitalDemodulator::get_ModulationType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ModulationType</b> method retrieves the modulation type for the signal.

## -parameters

### -param pModulationType [out]

Pointer that receives a <a href="/previous-versions/windows/desktop/mstv/modulationtype">ModulationType</a> variable indicating the modulation type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_modulationtype">IBDA_DigitalDemodulator::put_ModulationType</a>