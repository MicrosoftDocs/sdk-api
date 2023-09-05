---
UID: NF:bdaiface.IFrequencyMap.get_CountryCode
title: IFrequencyMap::get_CountryCode (bdaiface.h)
description: The get_CountryCode method returns the country/region code the Network Provider is currently using. The country/region code determines which frequency table the Network Provider loads.
helpviewer_keywords: ["IFrequencyMap interface [Microsoft TV Technologies]","get_CountryCode method","IFrequencyMap.get_CountryCode","IFrequencyMap::get_CountryCode","IFrequencyMapget_CountryCode","bdaiface/IFrequencyMap::get_CountryCode","get_CountryCode","get_CountryCode method [Microsoft TV Technologies]","get_CountryCode method [Microsoft TV Technologies]","IFrequencyMap interface","mstv.ifrequencymap_get_countrycode"]
old-location: mstv\ifrequencymap_get_countrycode.htm
tech.root: mstv
ms.assetid: 3f5e4109-e424-40be-9b3c-7eeef895e677
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_CountryCode method, IFrequencyMap.get_CountryCode, IFrequencyMap::get_CountryCode, IFrequencyMapget_CountryCode, bdaiface/IFrequencyMap::get_CountryCode, get_CountryCode, get_CountryCode method [Microsoft TV Technologies], get_CountryCode method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_countrycode
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
 - IFrequencyMap::get_CountryCode
 - bdaiface/IFrequencyMap::get_CountryCode
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
 - IFrequencyMap.get_CountryCode
---

# IFrequencyMap::get_CountryCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CountryCode</b> method returns the country/region code the Network Provider is currently using. The country/region code determines which frequency table the Network Provider loads.

## -parameters

### -param pulCountryCode [out]

Pointer to a variable that receives the country/region code.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

For a list of country/region codes, see <a href="/windows/desktop/DirectShow/country-region-assignments">Country/Region Assignments</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>