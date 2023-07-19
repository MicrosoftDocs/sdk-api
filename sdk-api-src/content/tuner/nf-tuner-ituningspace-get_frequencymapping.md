---
UID: NF:tuner.ITuningSpace.get_FrequencyMapping
title: ITuningSpace::get_FrequencyMapping (tuner.h)
description: The get_FrequencyMapping method retrieves the frequency mapping previously created by the network provider by a call to put_FrequencyMapping.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_FrequencyMapping method","ITuningSpace.get_FrequencyMapping","ITuningSpace::get_FrequencyMapping","ITuningSpaceget_FrequencyMapping","get_FrequencyMapping","get_FrequencyMapping method [Microsoft TV Technologies]","get_FrequencyMapping method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_frequencymapping","tuner/ITuningSpace::get_FrequencyMapping"]
old-location: mstv\ituningspace_get_frequencymapping.htm
tech.root: mstv
ms.assetid: 86f6f991-7ba6-4dcc-86bd-03e44c799c22
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_FrequencyMapping method, ITuningSpace.get_FrequencyMapping, ITuningSpace::get_FrequencyMapping, ITuningSpaceget_FrequencyMapping, get_FrequencyMapping, get_FrequencyMapping method [Microsoft TV Technologies], get_FrequencyMapping method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_frequencymapping, tuner/ITuningSpace::get_FrequencyMapping
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
 - ITuningSpace::get_FrequencyMapping
 - tuner/ITuningSpace::get_FrequencyMapping
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
 - ITuningSpace.get_FrequencyMapping
---

# ITuningSpace::get_FrequencyMapping


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FrequencyMapping</b> method retrieves the frequency mapping previously created by the network provider by a call to <b>put_FrequencyMapping</b>.

## -parameters

### -param pMapping [out]

Pointer to a variable that receives the frequency mappings created by the Network Provider filter.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The returned <b>BSTR</b> is treated as a binary blob. It is expected to contain embedded <b>NULL</b> values, and it may be formatted internally by the <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a>.

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>