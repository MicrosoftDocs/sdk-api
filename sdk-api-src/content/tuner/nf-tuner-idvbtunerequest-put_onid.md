---
UID: NF:tuner.IDVBTuneRequest.put_ONID
title: IDVBTuneRequest::put_ONID (tuner.h)
description: The put_ONID method sets the original network ID.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","put_ONID method","IDVBTuneRequest.put_ONID","IDVBTuneRequest::put_ONID","IDVBTuneRequestput_ONID","mstv.idvbtunerequest_put_onid","put_ONID","put_ONID method [Microsoft TV Technologies]","put_ONID method [Microsoft TV Technologies]","IDVBTuneRequest interface","tuner/IDVBTuneRequest::put_ONID"]
old-location: mstv\idvbtunerequest_put_onid.htm
tech.root: mstv
ms.assetid: 6f080aed-3a25-4464-ab74-27327a9f62a5
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],put_ONID method, IDVBTuneRequest.put_ONID, IDVBTuneRequest::put_ONID, IDVBTuneRequestput_ONID, mstv.idvbtunerequest_put_onid, put_ONID, put_ONID method [Microsoft TV Technologies], put_ONID method [Microsoft TV Technologies],IDVBTuneRequest interface, tuner/IDVBTuneRequest::put_ONID
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
 - IDVBTuneRequest::put_ONID
 - tuner/IDVBTuneRequest::put_ONID
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
 - IDVBTuneRequest.put_ONID
---

# IDVBTuneRequest::put_ONID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_ONID</b> method sets the original network ID.

## -parameters

### -param ONID [in]

The original network ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>