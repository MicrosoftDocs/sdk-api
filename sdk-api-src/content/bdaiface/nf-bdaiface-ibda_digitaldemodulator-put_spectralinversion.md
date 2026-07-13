---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_SpectralInversion
title: IBDA_DigitalDemodulator::put_SpectralInversion (bdaiface.h)
description: The put_SpectralInversion method specifies the spectral inversion value for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","put_SpectralInversion method","IBDA_DigitalDemodulator.put_SpectralInversion","IBDA_DigitalDemodulator::put_SpectralInversion","IBDA_DigitalDemodulatorput_SpectralInversion","bdaiface/IBDA_DigitalDemodulator::put_SpectralInversion","mstv.ibda_digitaldemodulator_put_spectralinversion","put_SpectralInversion","put_SpectralInversion method [Microsoft TV Technologies]","put_SpectralInversion method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface"]
old-location: mstv\ibda_digitaldemodulator_put_spectralinversion.htm
tech.root: mstv
ms.assetid: 6aabb829-5198-407f-a8f7-f99f87229560
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_SpectralInversion method, IBDA_DigitalDemodulator.put_SpectralInversion, IBDA_DigitalDemodulator::put_SpectralInversion, IBDA_DigitalDemodulatorput_SpectralInversion, bdaiface/IBDA_DigitalDemodulator::put_SpectralInversion, mstv.ibda_digitaldemodulator_put_spectralinversion, put_SpectralInversion, put_SpectralInversion method [Microsoft TV Technologies], put_SpectralInversion method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator::put_SpectralInversion
 - bdaiface/IBDA_DigitalDemodulator::put_SpectralInversion
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
 - IBDA_DigitalDemodulator.put_SpectralInversion
---

# IBDA_DigitalDemodulator::put_SpectralInversion


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SpectralInversion</b> method specifies the spectral inversion value for the signal.

## -parameters

### -param pSpectralInversion [in]

Pointer to a <a href="/previous-versions/windows/desktop/mstv/spectralinversion">SpectralInversion</a> variable.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/previous-versions/windows/desktop/mstv/spectralinversion">IBDA_DigitalDemodulator::get_SpectralInversion</a>