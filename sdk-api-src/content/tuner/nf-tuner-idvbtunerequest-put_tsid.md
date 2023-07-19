---
UID: NF:tuner.IDVBTuneRequest.put_TSID
title: IDVBTuneRequest::put_TSID (tuner.h)
description: The put_TSID method sets the transport stream ID.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","put_TSID method","IDVBTuneRequest.put_TSID","IDVBTuneRequest::put_TSID","IDVBTuneRequestput_TSID","mstv.idvbtunerequest_put_tsid","put_TSID","put_TSID method [Microsoft TV Technologies]","put_TSID method [Microsoft TV Technologies]","IDVBTuneRequest interface","tuner/IDVBTuneRequest::put_TSID"]
old-location: mstv\idvbtunerequest_put_tsid.htm
tech.root: mstv
ms.assetid: f72dce85-3584-40bc-ae7a-69c9914c13b9
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],put_TSID method, IDVBTuneRequest.put_TSID, IDVBTuneRequest::put_TSID, IDVBTuneRequestput_TSID, mstv.idvbtunerequest_put_tsid, put_TSID, put_TSID method [Microsoft TV Technologies], put_TSID method [Microsoft TV Technologies],IDVBTuneRequest interface, tuner/IDVBTuneRequest::put_TSID
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
 - IDVBTuneRequest::put_TSID
 - tuner/IDVBTuneRequest::put_TSID
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
 - IDVBTuneRequest.put_TSID
---

# IDVBTuneRequest::put_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TSID</b> method sets the transport stream ID.

## -parameters

### -param TSID [in]

The transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>