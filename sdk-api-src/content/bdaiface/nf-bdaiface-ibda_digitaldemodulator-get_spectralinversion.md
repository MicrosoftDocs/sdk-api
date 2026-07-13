---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_SpectralInversion
title: IBDA_DigitalDemodulator::get_SpectralInversion (bdaiface.h)
description: The get_SpectralInversion method retrieves the spectral inversion value for the signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","get_SpectralInversion method","IBDA_DigitalDemodulator.get_SpectralInversion","IBDA_DigitalDemodulator::get_SpectralInversion","IBDA_DigitalDemodulatorget_SpectralInversion","bdaiface/IBDA_DigitalDemodulator::get_SpectralInversion","get_SpectralInversion","get_SpectralInversion method [Microsoft TV Technologies]","get_SpectralInversion method [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface","mstv.ibda_digitaldemodulator_get_spectralinversion"]
old-location: mstv\ibda_digitaldemodulator_get_spectralinversion.htm
tech.root: mstv
ms.assetid: eaab17e3-8070-4f70-a31c-cd130edf1a4a
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_SpectralInversion method, IBDA_DigitalDemodulator.get_SpectralInversion, IBDA_DigitalDemodulator::get_SpectralInversion, IBDA_DigitalDemodulatorget_SpectralInversion, bdaiface/IBDA_DigitalDemodulator::get_SpectralInversion, get_SpectralInversion, get_SpectralInversion method [Microsoft TV Technologies], get_SpectralInversion method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_spectralinversion
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
 - IBDA_DigitalDemodulator::get_SpectralInversion
 - bdaiface/IBDA_DigitalDemodulator::get_SpectralInversion
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
 - IBDA_DigitalDemodulator.get_SpectralInversion
---

# IBDA_DigitalDemodulator::get_SpectralInversion


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SpectralInversion</b> method retrieves the spectral inversion value for the signal.

## -parameters

### -param pSpectralInversion [out]

Pointer that receives a <a href="/previous-versions/windows/desktop/mstv/spectralinversion">SpectralInversion</a> variable.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

For more information, see <b>KSPROPERTY_BDA_SPECTRAL_INVERSION</b> in the Windows DDK.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_spectralinversion">IBDA_DigitalDemodulator::put_SpectralInversion</a>