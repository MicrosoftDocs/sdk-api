---
UID: NF:tuner.IATSCLocator.get_TSID
title: IATSCLocator::get_TSID (tuner.h)
description: The get_TSID method retrieves the transport stream ID.
helpviewer_keywords: ["IATSCLocator interface [Microsoft TV Technologies]","get_TSID method","IATSCLocator.get_TSID","IATSCLocator::get_TSID","IATSCLocatorget_TSID","get_TSID","get_TSID method [Microsoft TV Technologies]","get_TSID method [Microsoft TV Technologies]","IATSCLocator interface","mstv.iatsclocator_get_tsid","tuner/IATSCLocator::get_TSID"]
old-location: mstv\iatsclocator_get_tsid.htm
tech.root: mstv
ms.assetid: e7cde550-742c-426c-a350-1d05b74f824d
ms.date: 12/05/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],get_TSID method, IATSCLocator.get_TSID, IATSCLocator::get_TSID, IATSCLocatorget_TSID, get_TSID, get_TSID method [Microsoft TV Technologies], get_TSID method [Microsoft TV Technologies],IATSCLocator interface, mstv.iatsclocator_get_tsid, tuner/IATSCLocator::get_TSID
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
 - IATSCLocator::get_TSID
 - tuner/IATSCLocator::get_TSID
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
 - IATSCLocator.get_TSID
---

# IATSCLocator::get_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TSID</b> method retrieves the transport stream ID.

## -parameters

### -param TSID [out]

Receives the transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This property is not required for tuning. It will be set by the BDA Transport Information Filter (TIF) when the signal is acquired. This property is not used by the application but may be used by one or more of the receiver filters. For example, a TIF may use this to determine whether the transport stream has changed from what was originally tuned and generate events that cause re-acquisition of the requested program.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator Interface</a>