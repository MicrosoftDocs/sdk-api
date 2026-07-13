---
UID: NF:tuner.IAnalogRadioTuningSpace2.put_CountryCode
title: IAnalogRadioTuningSpace2::put_CountryCode (tuner.h)
description: This topic applies to Windows XP Media Center Edition 2004 and later.
helpviewer_keywords: ["IAnalogRadioTuningSpace2 interface [Microsoft TV Technologies]","put_CountryCode method","IAnalogRadioTuningSpace2.put_CountryCode","IAnalogRadioTuningSpace2::put_CountryCode","IAnalogRadioTuningSpace2put_CountryCode","mstv.ianalogradiotuningspace2_put_countrycode","put_CountryCode","put_CountryCode method [Microsoft TV Technologies]","put_CountryCode method [Microsoft TV Technologies]","IAnalogRadioTuningSpace2 interface","tuner/IAnalogRadioTuningSpace2::put_CountryCode"]
old-location: mstv\ianalogradiotuningspace2_put_countrycode.htm
tech.root: mstv
ms.assetid: 89aecae6-42c0-4130-b381-986c0327fe5d
ms.date: 12/05/2018
ms.keywords: IAnalogRadioTuningSpace2 interface [Microsoft TV Technologies],put_CountryCode method, IAnalogRadioTuningSpace2.put_CountryCode, IAnalogRadioTuningSpace2::put_CountryCode, IAnalogRadioTuningSpace2put_CountryCode, mstv.ianalogradiotuningspace2_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IAnalogRadioTuningSpace2 interface, tuner/IAnalogRadioTuningSpace2::put_CountryCode
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAnalogRadioTuningSpace2::put_CountryCode
 - tuner/IAnalogRadioTuningSpace2::put_CountryCode
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
 - IAnalogRadioTuningSpace2.put_CountryCode
---

# IAnalogRadioTuningSpace2::put_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Media Center Edition 2004 and later.
        



The <b>put_CountryCode</b> method sets the country/region code of the tuning space (based on TAPI country/region codes).

## -parameters

### -param NewCountryCodeVal [in]

The country/region code.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogradiotuningspace2">IAnalogRadioTuningSpace2 Interface</a>