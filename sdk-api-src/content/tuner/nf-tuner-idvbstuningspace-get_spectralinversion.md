---
UID: NF:tuner.IDVBSTuningSpace.get_SpectralInversion
title: IDVBSTuningSpace::get_SpectralInversion (tuner.h)
description: The get_SpectralInversion method retrieves an integer indicating the spectral inversion.
helpviewer_keywords: ["IDVBSTuningSpace interface [Microsoft TV Technologies]","get_SpectralInversion method","IDVBSTuningSpace.get_SpectralInversion","IDVBSTuningSpace::get_SpectralInversion","IDVBSTuningSpaceget_SpectralInversion","get_SpectralInversion","get_SpectralInversion method [Microsoft TV Technologies]","get_SpectralInversion method [Microsoft TV Technologies]","IDVBSTuningSpace interface","mstv.idvbstuningspace_get_spectralinversion","tuner/IDVBSTuningSpace::get_SpectralInversion"]
old-location: mstv\idvbstuningspace_get_spectralinversion.htm
tech.root: mstv
ms.assetid: 68374808-2999-4196-9b2b-b6c97308b041
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace interface [Microsoft TV Technologies],get_SpectralInversion method, IDVBSTuningSpace.get_SpectralInversion, IDVBSTuningSpace::get_SpectralInversion, IDVBSTuningSpaceget_SpectralInversion, get_SpectralInversion, get_SpectralInversion method [Microsoft TV Technologies], get_SpectralInversion method [Microsoft TV Technologies],IDVBSTuningSpace interface, mstv.idvbstuningspace_get_spectralinversion, tuner/IDVBSTuningSpace::get_SpectralInversion
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IDVBSTuningSpace::get_SpectralInversion
 - tuner/IDVBSTuningSpace::get_SpectralInversion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBSTuningSpace.get_SpectralInversion
---

# IDVBSTuningSpace::get_SpectralInversion


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SpectralInversion</b> method retrieves an integer indicating the spectral inversion.

## -parameters

### -param SpectralInversionVal [out]

Receives the spectral inversion.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbstuningspace">IDVBSTuningSpace Interface</a>