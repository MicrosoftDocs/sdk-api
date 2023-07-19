---
UID: NF:tuner.IAnalogTVTuningSpace.get_CountryCode
title: IAnalogTVTuningSpace::get_CountryCode (tuner.h)
description: The get_CountryCode method gets the country/region code of the tuning space (based on TAPI country/region codes).
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","get_CountryCode method","IAnalogTVTuningSpace.get_CountryCode","IAnalogTVTuningSpace::get_CountryCode","IAnalogTVTuningSpaceget_CountryCode","get_CountryCode","get_CountryCode method [Microsoft TV Technologies]","get_CountryCode method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","mstv.ianalogtvtuningspace_get_countrycode","tuner/IAnalogTVTuningSpace::get_CountryCode"]
old-location: mstv\ianalogtvtuningspace_get_countrycode.htm
tech.root: mstv
ms.assetid: f74f31cc-8e3a-41b8-bf27-f60b9cbcfcdb
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],get_CountryCode method, IAnalogTVTuningSpace.get_CountryCode, IAnalogTVTuningSpace::get_CountryCode, IAnalogTVTuningSpaceget_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, mstv.ianalogtvtuningspace_get_countrycode, tuner/IAnalogTVTuningSpace::get_CountryCode
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
 - IAnalogTVTuningSpace::get_CountryCode
 - tuner/IAnalogTVTuningSpace::get_CountryCode
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
 - IAnalogTVTuningSpace.get_CountryCode
---

# IAnalogTVTuningSpace::get_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CountryCode</b> method gets the country/region code of the tuning space (based on TAPI country/region codes).

## -parameters

### -param CountryCodeVal [out]

Receives the value for the country/region code.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The tuner can use the country/region code to locate a likely channel for frequency mapping.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>