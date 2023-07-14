---
UID: NF:tuner.ILocator.get_CarrierFrequency
title: ILocator::get_CarrierFrequency (tuner.h)
description: The get_CarrierFrequency method gets the frequency of the RF signal.
helpviewer_keywords: ["ILocator interface [Microsoft TV Technologies]","get_CarrierFrequency method","ILocator.get_CarrierFrequency","ILocator::get_CarrierFrequency","ILocatorget_CarrierFrequency","get_CarrierFrequency","get_CarrierFrequency method [Microsoft TV Technologies]","get_CarrierFrequency method [Microsoft TV Technologies]","ILocator interface","mstv.ilocator_get_carrierfrequency","tuner/ILocator::get_CarrierFrequency"]
old-location: mstv\ilocator_get_carrierfrequency.htm
tech.root: mstv
ms.assetid: 15f6d54c-81c8-40d3-937f-c54102f3a230
ms.date: 12/05/2018
ms.keywords: ILocator interface [Microsoft TV Technologies],get_CarrierFrequency method, ILocator.get_CarrierFrequency, ILocator::get_CarrierFrequency, ILocatorget_CarrierFrequency, get_CarrierFrequency, get_CarrierFrequency method [Microsoft TV Technologies], get_CarrierFrequency method [Microsoft TV Technologies],ILocator interface, mstv.ilocator_get_carrierfrequency, tuner/ILocator::get_CarrierFrequency
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
 - ILocator::get_CarrierFrequency
 - tuner/ILocator::get_CarrierFrequency
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
 - ILocator.get_CarrierFrequency
---

# ILocator::get_CarrierFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CarrierFrequency</b> method gets the frequency of the RF signal.

## -parameters

### -param Frequency [out]

Receives the frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator Interface</a>