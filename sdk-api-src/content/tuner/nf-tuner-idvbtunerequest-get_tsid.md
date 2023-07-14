---
UID: NF:tuner.IDVBTuneRequest.get_TSID
title: IDVBTuneRequest::get_TSID (tuner.h)
description: The get_TSID method retrieves the transport stream ID.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","get_TSID method","IDVBTuneRequest.get_TSID","IDVBTuneRequest::get_TSID","IDVBTuneRequestget_TSID","get_TSID","get_TSID method [Microsoft TV Technologies]","get_TSID method [Microsoft TV Technologies]","IDVBTuneRequest interface","mstv.idvbtunerequest_get_tsid","tuner/IDVBTuneRequest::get_TSID"]
old-location: mstv\idvbtunerequest_get_tsid.htm
tech.root: mstv
ms.assetid: 3bbc0fd0-5b4d-4701-b3ca-7581efff9e71
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],get_TSID method, IDVBTuneRequest.get_TSID, IDVBTuneRequest::get_TSID, IDVBTuneRequestget_TSID, get_TSID, get_TSID method [Microsoft TV Technologies], get_TSID method [Microsoft TV Technologies],IDVBTuneRequest interface, mstv.idvbtunerequest_get_tsid, tuner/IDVBTuneRequest::get_TSID
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
 - IDVBTuneRequest::get_TSID
 - tuner/IDVBTuneRequest::get_TSID
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
 - IDVBTuneRequest.get_TSID
---

# IDVBTuneRequest::get_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TSID</b> method retrieves the transport stream ID.

## -parameters

### -param TSID [out]

Receives the transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>