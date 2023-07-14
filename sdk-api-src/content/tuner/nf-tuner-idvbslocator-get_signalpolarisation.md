---
UID: NF:tuner.IDVBSLocator.get_SignalPolarisation
title: IDVBSLocator::get_SignalPolarisation (tuner.h)
description: The get_SignalPolarisation method retrieves the signal polarisation.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","get_SignalPolarisation method","IDVBSLocator.get_SignalPolarisation","IDVBSLocator::get_SignalPolarisation","IDVBSLocatorget_SignalPolarisation","get_SignalPolarisation","get_SignalPolarisation method [Microsoft TV Technologies]","get_SignalPolarisation method [Microsoft TV Technologies]","IDVBSLocator interface","mstv.idvbslocator_get_signalpolarisation","tuner/IDVBSLocator::get_SignalPolarisation"]
old-location: mstv\idvbslocator_get_signalpolarisation.htm
tech.root: mstv
ms.assetid: adb9d7b6-5876-4b3f-9d82-f5e740feb1eb
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_SignalPolarisation method, IDVBSLocator.get_SignalPolarisation, IDVBSLocator::get_SignalPolarisation, IDVBSLocatorget_SignalPolarisation, get_SignalPolarisation, get_SignalPolarisation method [Microsoft TV Technologies], get_SignalPolarisation method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_signalpolarisation, tuner/IDVBSLocator::get_SignalPolarisation
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
 - IDVBSLocator::get_SignalPolarisation
 - tuner/IDVBSLocator::get_SignalPolarisation
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
 - IDVBSLocator.get_SignalPolarisation
---

# IDVBSLocator::get_SignalPolarisation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalPolarisation</b> method retrieves the signal polarisation.

## -parameters

### -param PolarisationVal [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/polarisation">Polarisation</a> that receives the polarisation value.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method and the associated enumeration type use the British spelling for "polarisation" to maintain consistency with standards documentation.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>