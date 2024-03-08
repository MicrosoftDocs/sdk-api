---
UID: NF:tuner.IDVBTuneRequest.get_ONID
title: IDVBTuneRequest::get_ONID (tuner.h)
description: The get_ONID method retrieves the original network ID.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","get_ONID method","IDVBTuneRequest.get_ONID","IDVBTuneRequest::get_ONID","IDVBTuneRequestget_ONID","get_ONID","get_ONID method [Microsoft TV Technologies]","get_ONID method [Microsoft TV Technologies]","IDVBTuneRequest interface","mstv.idvbtunerequest_get_onid","tuner/IDVBTuneRequest::get_ONID"]
old-location: mstv\idvbtunerequest_get_onid.htm
tech.root: mstv
ms.assetid: 24cfc4bb-7df0-4380-9322-4bec6e8a2385
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],get_ONID method, IDVBTuneRequest.get_ONID, IDVBTuneRequest::get_ONID, IDVBTuneRequestget_ONID, get_ONID, get_ONID method [Microsoft TV Technologies], get_ONID method [Microsoft TV Technologies],IDVBTuneRequest interface, mstv.idvbtunerequest_get_onid, tuner/IDVBTuneRequest::get_ONID
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
 - IDVBTuneRequest::get_ONID
 - tuner/IDVBTuneRequest::get_ONID
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
 - IDVBTuneRequest.get_ONID
---

# IDVBTuneRequest::get_ONID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ONID</b> method retrieves the original network ID.

## -parameters

### -param ONID [out]

Receives the original network ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>