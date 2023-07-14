---
UID: NF:tuner.ILocator.put_CarrierFrequency
title: ILocator::put_CarrierFrequency (tuner.h)
description: The put_CarrierFrequency method sets the frequency of the RF signal.
helpviewer_keywords: ["ILocator interface [Microsoft TV Technologies]","put_CarrierFrequency method","ILocator.put_CarrierFrequency","ILocator::put_CarrierFrequency","ILocatorput_CarrierFrequency","mstv.ilocator_put_carrierfrequency","put_CarrierFrequency","put_CarrierFrequency method [Microsoft TV Technologies]","put_CarrierFrequency method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_CarrierFrequency"]
old-location: mstv\ilocator_put_carrierfrequency.htm
tech.root: mstv
ms.assetid: 74617c08-dabc-48d7-a9da-d1631d7df961
ms.date: 12/05/2018
ms.keywords: ILocator interface [Microsoft TV Technologies],put_CarrierFrequency method, ILocator.put_CarrierFrequency, ILocator::put_CarrierFrequency, ILocatorput_CarrierFrequency, mstv.ilocator_put_carrierfrequency, put_CarrierFrequency, put_CarrierFrequency method [Microsoft TV Technologies], put_CarrierFrequency method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_CarrierFrequency
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
 - ILocator::put_CarrierFrequency
 - tuner/ILocator::put_CarrierFrequency
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
 - ILocator.put_CarrierFrequency
---

# ILocator::put_CarrierFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_CarrierFrequency</b> method sets the frequency of the RF signal.

## -parameters

### -param Frequency [in]

The frequency, in kilohertz (kHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator Interface</a>