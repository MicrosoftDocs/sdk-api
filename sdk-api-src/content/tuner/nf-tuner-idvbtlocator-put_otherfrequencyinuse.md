---
UID: NF:tuner.IDVBTLocator.put_OtherFrequencyInUse
title: IDVBTLocator::put_OtherFrequencyInUse (tuner.h)
description: The put_OtherFrequencyInUse method specifies whether the frequency is being used by another DVB-T broadcaster.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_OtherFrequencyInUse method","IDVBTLocator.put_OtherFrequencyInUse","IDVBTLocator::put_OtherFrequencyInUse","IDVBTLocatorput_OtherFrequencyInUse","mstv.idvbtlocator_put_otherfrequencyinuse","put_OtherFrequencyInUse","put_OtherFrequencyInUse method [Microsoft TV Technologies]","put_OtherFrequencyInUse method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_OtherFrequencyInUse"]
old-location: mstv\idvbtlocator_put_otherfrequencyinuse.htm
tech.root: mstv
ms.assetid: ab9504f9-469d-476d-aad8-f9534f6b41bf
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_OtherFrequencyInUse method, IDVBTLocator.put_OtherFrequencyInUse, IDVBTLocator::put_OtherFrequencyInUse, IDVBTLocatorput_OtherFrequencyInUse, mstv.idvbtlocator_put_otherfrequencyinuse, put_OtherFrequencyInUse, put_OtherFrequencyInUse method [Microsoft TV Technologies], put_OtherFrequencyInUse method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_OtherFrequencyInUse
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
 - IDVBTLocator::put_OtherFrequencyInUse
 - tuner/IDVBTLocator::put_OtherFrequencyInUse
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
 - IDVBTLocator.put_OtherFrequencyInUse
---

# IDVBTLocator::put_OtherFrequencyInUse


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OtherFrequencyInUse</b> method specifies whether the frequency is being used by another DVB-T broadcaster.

## -parameters

### -param OtherFrequencyInUseVal [in]

Specify VARIANT_TRUE if the frequency is being used by another DVB-T broadcaster, or VARIANT_FALSE otherwise.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>