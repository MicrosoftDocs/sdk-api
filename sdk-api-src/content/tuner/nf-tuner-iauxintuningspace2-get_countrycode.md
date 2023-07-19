---
UID: NF:tuner.IAuxInTuningSpace2.get_CountryCode
title: IAuxInTuningSpace2::get_CountryCode (tuner.h)
description: This topic applies to Windows XP Media Center Edition 2004 and later.
helpviewer_keywords: ["IAuxInTuningSpace2 interface [Microsoft TV Technologies]","get_CountryCode method","IAuxInTuningSpace2.get_CountryCode","IAuxInTuningSpace2::get_CountryCode","IAuxInTuningSpace2get_CountryCode","get_CountryCode","get_CountryCode method [Microsoft TV Technologies]","get_CountryCode method [Microsoft TV Technologies]","IAuxInTuningSpace2 interface","mstv.iauxintuningspace2_get_countrycode","tuner/IAuxInTuningSpace2::get_CountryCode"]
old-location: mstv\iauxintuningspace2_get_countrycode.htm
tech.root: mstv
ms.assetid: dffd3ad2-2caa-4041-9e24-024050414a87
ms.date: 12/05/2018
ms.keywords: IAuxInTuningSpace2 interface [Microsoft TV Technologies],get_CountryCode method, IAuxInTuningSpace2.get_CountryCode, IAuxInTuningSpace2::get_CountryCode, IAuxInTuningSpace2get_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IAuxInTuningSpace2 interface, mstv.iauxintuningspace2_get_countrycode, tuner/IAuxInTuningSpace2::get_CountryCode
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
 - IAuxInTuningSpace2::get_CountryCode
 - tuner/IAuxInTuningSpace2::get_CountryCode
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
 - IAuxInTuningSpace2.get_CountryCode
---

# IAuxInTuningSpace2::get_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Media Center Edition 2004 and later.
        



The <b>get_CountryCode</b> method gets the country/region code of the tuning space (based on TAPI country/region codes).

## -parameters

### -param CountryCodeVal [out]

Pointer to a variable that receives the country/region code.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iauxintuningspace2">IAuxInTuningSpace2 Interface</a>