---
UID: NF:tuner.IDVBTLocator.get_OtherFrequencyInUse
title: IDVBTLocator::get_OtherFrequencyInUse (tuner.h)
description: The get_OtherFrequencyInUse method indicates whether the frequency is being used by another DVB-T broadcaster.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_OtherFrequencyInUse method","IDVBTLocator.get_OtherFrequencyInUse","IDVBTLocator::get_OtherFrequencyInUse","IDVBTLocatorget_OtherFrequencyInUse","get_OtherFrequencyInUse","get_OtherFrequencyInUse method [Microsoft TV Technologies]","get_OtherFrequencyInUse method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_otherfrequencyinuse","tuner/IDVBTLocator::get_OtherFrequencyInUse"]
old-location: mstv\idvbtlocator_get_otherfrequencyinuse.htm
tech.root: mstv
ms.assetid: fcb39760-901f-4c62-a517-bee7ea96f8d9
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_OtherFrequencyInUse method, IDVBTLocator.get_OtherFrequencyInUse, IDVBTLocator::get_OtherFrequencyInUse, IDVBTLocatorget_OtherFrequencyInUse, get_OtherFrequencyInUse, get_OtherFrequencyInUse method [Microsoft TV Technologies], get_OtherFrequencyInUse method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_otherfrequencyinuse, tuner/IDVBTLocator::get_OtherFrequencyInUse
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
 - IDVBTLocator::get_OtherFrequencyInUse
 - tuner/IDVBTLocator::get_OtherFrequencyInUse
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
 - IDVBTLocator.get_OtherFrequencyInUse
---

# IDVBTLocator::get_OtherFrequencyInUse


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OtherFrequencyInUse</b> method indicates whether the frequency is being used by another DVB-T broadcaster.

## -parameters

### -param OtherFrequencyInUseVal [out]

Receives that value VARIANT_TRUE if the frequency is being used by another DVB-T broadcaster, or VARIANT_FALSE otherwise.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>