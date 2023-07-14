---
UID: NF:bdaiface.IFrequencyMap.put_CountryCode
title: IFrequencyMap::put_CountryCode (bdaiface.h)
description: The put_CountryCode method sets the country/region code on the Network Provider filter.
helpviewer_keywords: ["IFrequencyMap interface [Microsoft TV Technologies]","put_CountryCode method","IFrequencyMap.put_CountryCode","IFrequencyMap::put_CountryCode","IFrequencyMapput_CountryCode","bdaiface/IFrequencyMap::put_CountryCode","mstv.ifrequencymap_put_countrycode","put_CountryCode","put_CountryCode method [Microsoft TV Technologies]","put_CountryCode method [Microsoft TV Technologies]","IFrequencyMap interface"]
old-location: mstv\ifrequencymap_put_countrycode.htm
tech.root: mstv
ms.assetid: 8473e292-b47b-4c1a-b45e-b8acf0e36263
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],put_CountryCode method, IFrequencyMap.put_CountryCode, IFrequencyMap::put_CountryCode, IFrequencyMapput_CountryCode, bdaiface/IFrequencyMap::put_CountryCode, mstv.ifrequencymap_put_countrycode, put_CountryCode, put_CountryCode method [Microsoft TV Technologies], put_CountryCode method [Microsoft TV Technologies],IFrequencyMap interface
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
 - IFrequencyMap::put_CountryCode
 - bdaiface/IFrequencyMap::put_CountryCode
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
 - IFrequencyMap.put_CountryCode
---

# IFrequencyMap::put_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_CountryCode</b> method sets the country/region code on the Network Provider filter.

## -parameters

### -param ulCountryCode [in]

Specifies the country/region code.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the method succeeds, the Network Provider loads the frequency table for the specified country/region code. It uses this table in all subsequent calls to <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> methods.

If the country/region code does not match an existing frequency table, the method fails and the Network Provider continues to use the previous table. However, it stores the new country/region code, and the application can create a new frequency table by calling the <b>put_FrequencyMapping</b> method. This behavior enables an application to define new country/region codes with new frequency tables.

For a list of existing country/region codes, see <a href="/windows/desktop/DirectShow/country-region-assignments">Country/Region Assignments</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>