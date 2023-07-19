---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_ModulationType
title: IBDA_DigitalDemodulator::put_ModulationType (bdaiface.h)
description: The put_ModulationType method specifies the modulation type for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_ModulationType method","IBDA_DigitalDemodulator.put_ModulationType","IBDA_DigitalDemodulator::put_ModulationType","IBDA_DigitalDemodulatorput_ModulationType","bdaiface/IBDA_DigitalDemodulator::put_ModulationType","mstv.ibda_digitaldemodulator_put_modulationtype","put_ModulationType","put_ModulationType method [Microsoft TV Technologies]","put_ModulationType method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_modulationtype.htm
tech.root: mstv
ms.assetid: 9e2bf33f-b139-4455-ad49-c75e52f31083
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_ModulationType method, IBDA_DigitalDemodulator.put_ModulationType, IBDA_DigitalDemodulator::put_ModulationType, IBDA_DigitalDemodulatorput_ModulationType, bdaiface/IBDA_DigitalDemodulator::put_ModulationType, mstv.ibda_digitaldemodulator_put_modulationtype, put_ModulationType, put_ModulationType method [Microsoft TV Technologies], put_ModulationType method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_ModulationType
 - bdaiface/IBDA_DigitalDemodulator::put_ModulationType
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
 - IBDA_DigitalDemodulator.put_ModulationType
---

# IBDA_DigitalDemodulator::put_ModulationType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_ModulationType</b> method specifies the modulation type for the signal.

## -parameters

### -param pModulationType [in]

Pointer to a <a href="/previous-versions/windows/desktop/mstv/modulationtype">ModulationType</a> variable that specifies the modulation type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/previous-versions/windows/desktop/mstv/modulationtype">IBDA_DigitalDemodulator::get_ModulationType</a>