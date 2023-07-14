---
UID: NF:bdaiface.IFrequencyMap.get_DefaultFrequencyMapping
title: IFrequencyMap::get_DefaultFrequencyMapping (bdaiface.h)
description: The get_DefaultFrequencyMapping method returns the default frequency table for a given country/region code.
helpviewer_keywords: ["IFrequencyMap interface [Microsoft TV Technologies]","get_DefaultFrequencyMapping method","IFrequencyMap.get_DefaultFrequencyMapping","IFrequencyMap::get_DefaultFrequencyMapping","IFrequencyMapget_DefaultMapping","bdaiface/IFrequencyMap::get_DefaultFrequencyMapping","get_DefaultFrequencyMapping","get_DefaultFrequencyMapping method [Microsoft TV Technologies]","get_DefaultFrequencyMapping method [Microsoft TV Technologies]","IFrequencyMap interface","mstv.ifrequencymap_get_defaultfrequencymapping"]
old-location: mstv\ifrequencymap_get_defaultfrequencymapping.htm
tech.root: mstv
ms.assetid: 67057c70-cb4d-4828-ad97-cf0181bd8cfe
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],get_DefaultFrequencyMapping method, IFrequencyMap.get_DefaultFrequencyMapping, IFrequencyMap::get_DefaultFrequencyMapping, IFrequencyMapget_DefaultMapping, bdaiface/IFrequencyMap::get_DefaultFrequencyMapping, get_DefaultFrequencyMapping, get_DefaultFrequencyMapping method [Microsoft TV Technologies], get_DefaultFrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface, mstv.ifrequencymap_get_defaultfrequencymapping
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
 - IFrequencyMap::get_DefaultFrequencyMapping
 - bdaiface/IFrequencyMap::get_DefaultFrequencyMapping
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
 - IFrequencyMap.get_DefaultFrequencyMapping
---

# IFrequencyMap::get_DefaultFrequencyMapping


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DefaultFrequencyMapping</b> method returns the default frequency table for a given country/region code. This method returns the frequency table, but does not set the country/region code on Network Provider. The Network Provider continues to use the same frequency table it was using before the method was called.

## -parameters

### -param ulCountryCode [in]

Specifies the country/region code.

### -param pulCount [out]

Pointer to a variable that receives the size of the frequency table.

### -param ppulList [out]

Pointer to a variable that receives the address of the frequency table. The frequency table is an array of size <i>pulCount</i>, allocated by the method. The caller must free the array by calling <b>CoTaskMemFree</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Each entry in the frequency table is a tuning frequency, in kilohertz (kHz).

For a list of country/region codes, see <a href="/windows/desktop/DirectShow/country-region-assignments">Country/Region Assignments</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>