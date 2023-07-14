---
UID: NF:tuner.IDVBTuneRequest.get_SID
title: IDVBTuneRequest::get_SID (tuner.h)
description: The get_SID method retrieves the service ID for the network.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","get_SID method","IDVBTuneRequest.get_SID","IDVBTuneRequest::get_SID","IDVBTuneRequestget_SID","get_SID","get_SID method [Microsoft TV Technologies]","get_SID method [Microsoft TV Technologies]","IDVBTuneRequest interface","mstv.idvbtunerequest_get_sid","tuner/IDVBTuneRequest::get_SID"]
old-location: mstv\idvbtunerequest_get_sid.htm
tech.root: mstv
ms.assetid: 2ddd5eec-c8bc-4f26-8acd-cf42876345ad
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],get_SID method, IDVBTuneRequest.get_SID, IDVBTuneRequest::get_SID, IDVBTuneRequestget_SID, get_SID, get_SID method [Microsoft TV Technologies], get_SID method [Microsoft TV Technologies],IDVBTuneRequest interface, mstv.idvbtunerequest_get_sid, tuner/IDVBTuneRequest::get_SID
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
 - IDVBTuneRequest::get_SID
 - tuner/IDVBTuneRequest::get_SID
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
 - IDVBTuneRequest.get_SID
---

# IDVBTuneRequest::get_SID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SID</b> method retrieves the service ID for the network.

## -parameters

### -param SID [out]

Receives the service ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>