---
UID: NF:tuner.ITuningSpace.put_FrequencyMapping
title: ITuningSpace::put_FrequencyMapping (tuner.h)
description: The put_FrequencyMapping method creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","put_FrequencyMapping method","ITuningSpace.put_FrequencyMapping","ITuningSpace::put_FrequencyMapping","ITuningSpaceput_FrequencyMapping","mstv.ituningspace_put_frequencymapping","put_FrequencyMapping","put_FrequencyMapping method [Microsoft TV Technologies]","put_FrequencyMapping method [Microsoft TV Technologies]","ITuningSpace interface","tuner/ITuningSpace::put_FrequencyMapping"]
old-location: mstv\ituningspace_put_frequencymapping.htm
tech.root: mstv
ms.assetid: 665ab139-773c-4e02-896f-2f97063a786f
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_FrequencyMapping method, ITuningSpace.put_FrequencyMapping, ITuningSpace::put_FrequencyMapping, ITuningSpaceput_FrequencyMapping, mstv.ituningspace_put_frequencymapping, put_FrequencyMapping, put_FrequencyMapping method [Microsoft TV Technologies], put_FrequencyMapping method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_FrequencyMapping
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
 - ITuningSpace::put_FrequencyMapping
 - tuner/ITuningSpace::put_FrequencyMapping
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
 - ITuningSpace.put_FrequencyMapping
---

# ITuningSpace::put_FrequencyMapping


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FrequencyMapping</b> method creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.

## -parameters

### -param Mapping [in]

<b>BSTR</b> that contains the frequency mappings.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is used by the network provider to store a string that contains the frequency mappings.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>