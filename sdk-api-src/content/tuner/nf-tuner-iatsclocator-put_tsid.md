---
UID: NF:tuner.IATSCLocator.put_TSID
title: IATSCLocator::put_TSID (tuner.h)
description: The put_TSID method sets the transport stream ID.
helpviewer_keywords: ["IATSCLocator interface [Microsoft TV Technologies]","put_TSID method","IATSCLocator.put_TSID","IATSCLocator::put_TSID","IATSCLocatorput_TSID","mstv.iatsclocator_put_tsid","put_TSID","put_TSID method [Microsoft TV Technologies]","put_TSID method [Microsoft TV Technologies]","IATSCLocator interface","tuner/IATSCLocator::put_TSID"]
old-location: mstv\iatsclocator_put_tsid.htm
tech.root: mstv
ms.assetid: 1864d2e7-0d4a-44b6-a9db-11f6efcd6986
ms.date: 12/05/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],put_TSID method, IATSCLocator.put_TSID, IATSCLocator::put_TSID, IATSCLocatorput_TSID, mstv.iatsclocator_put_tsid, put_TSID, put_TSID method [Microsoft TV Technologies], put_TSID method [Microsoft TV Technologies],IATSCLocator interface, tuner/IATSCLocator::put_TSID
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
 - IATSCLocator::put_TSID
 - tuner/IATSCLocator::put_TSID
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
 - IATSCLocator.put_TSID
---

# IATSCLocator::put_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TSID</b> method sets the transport stream ID.

## -parameters

### -param TSID [in]

The transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This property is optional.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator Interface</a>