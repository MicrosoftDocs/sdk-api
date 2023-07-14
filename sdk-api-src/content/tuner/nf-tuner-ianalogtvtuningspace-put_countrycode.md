---
UID: NF:tuner.IAnalogTVTuningSpace.put_CountryCode
title: IAnalogTVTuningSpace::put_CountryCode (tuner.h)
description: The put_CountryCode method sets the country/region code of the tuning space (based on TAPI country/region codes).
helpviewer_keywords: ["IAnalogTVTuningSpace interface [Microsoft TV Technologies]","put_CountryCode method","IAnalogTVTuningSpace.put_CountryCode","IAnalogTVTuningSpace::put_CountryCode","IAnalogTVTuningSpaceput_CountryCode","mstv.ianalogtvtuningspace_put_countrycode","put_CountryCode","put_CountryCode method [Microsoft TV Technologies]","put_CountryCode method [Microsoft TV Technologies]","IAnalogTVTuningSpace interface","tuner/IAnalogTVTuningSpace::put_CountryCode"]
old-location: mstv\ianalogtvtuningspace_put_countrycode.htm
tech.root: mstv
ms.assetid: eb53bdfe-6293-41f3-8945-5f960193df9e
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace interface [Microsoft TV Technologies],put_CountryCode method, IAnalogTVTuningSpace.put_CountryCode, IAnalogTVTuningSpace::put_CountryCode, IAnalogTVTuningSpaceput_CountryCode, mstv.ianalogtvtuningspace_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IAnalogTVTuningSpace interface, tuner/IAnalogTVTuningSpace::put_CountryCode
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
 - IAnalogTVTuningSpace::put_CountryCode
 - tuner/IAnalogTVTuningSpace::put_CountryCode
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
 - IAnalogTVTuningSpace.put_CountryCode
---

# IAnalogTVTuningSpace::put_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_CountryCode</b> method sets the country/region code of the tuning space (based on TAPI country/region codes).

## -parameters

### -param NewCountryCodeVal [in]

The country/region code.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The tuner can use the country/region code to locate a likely channel for frequency mapping.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace Interface</a>