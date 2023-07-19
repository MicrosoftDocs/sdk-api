---
UID: NF:tuner.IDVBTLocator.get_Bandwidth
title: IDVBTLocator::get_Bandwidth (tuner.h)
description: The get_Bandwidth method retrieves the bandwidth of the frequency.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_Bandwidth method","IDVBTLocator.get_Bandwidth","IDVBTLocator::get_Bandwidth","IDVBTLocatorget_Bandwidth","get_Bandwidth","get_Bandwidth method [Microsoft TV Technologies]","get_Bandwidth method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_bandwidth","tuner/IDVBTLocator::get_Bandwidth"]
old-location: mstv\idvbtlocator_get_bandwidth.htm
tech.root: mstv
ms.assetid: 7483d876-fdcc-4eee-b4f3-338846a159c0
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_Bandwidth method, IDVBTLocator.get_Bandwidth, IDVBTLocator::get_Bandwidth, IDVBTLocatorget_Bandwidth, get_Bandwidth, get_Bandwidth method [Microsoft TV Technologies], get_Bandwidth method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_bandwidth, tuner/IDVBTLocator::get_Bandwidth
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
 - IDVBTLocator::get_Bandwidth
 - tuner/IDVBTLocator::get_Bandwidth
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
 - IDVBTLocator.get_Bandwidth
---

# IDVBTLocator::get_Bandwidth


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Bandwidth</b> method retrieves the bandwidth of the frequency.

## -parameters

### -param BandWidthVal [out]

Receives the bandwidth, in megahertz (MHz).

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The bandwidth is determined by the bandwidth field in the DVB terrestrial delivery system descriptor, as defined in EN 300 468. Valid values are 7 or 8.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>