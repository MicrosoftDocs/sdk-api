---
UID: NF:tuner.IDVBTuneRequest.put_SID
title: IDVBTuneRequest::put_SID (tuner.h)
description: The put_SID method sets the service ID.
helpviewer_keywords: ["IDVBTuneRequest interface [Microsoft TV Technologies]","put_SID method","IDVBTuneRequest.put_SID","IDVBTuneRequest::put_SID","IDVBTuneRequestput_SID","mstv.idvbtunerequest_put_sid","put_SID","put_SID method [Microsoft TV Technologies]","put_SID method [Microsoft TV Technologies]","IDVBTuneRequest interface","tuner/IDVBTuneRequest::put_SID"]
old-location: mstv\idvbtunerequest_put_sid.htm
tech.root: mstv
ms.assetid: f521ab2d-5c56-4aff-a0a3-ac94b8676363
ms.date: 12/05/2018
ms.keywords: IDVBTuneRequest interface [Microsoft TV Technologies],put_SID method, IDVBTuneRequest.put_SID, IDVBTuneRequest::put_SID, IDVBTuneRequestput_SID, mstv.idvbtunerequest_put_sid, put_SID, put_SID method [Microsoft TV Technologies], put_SID method [Microsoft TV Technologies],IDVBTuneRequest interface, tuner/IDVBTuneRequest::put_SID
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
 - IDVBTuneRequest::put_SID
 - tuner/IDVBTuneRequest::put_SID
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
 - IDVBTuneRequest.put_SID
---

# IDVBTuneRequest::put_SID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SID</b> method sets the service ID.

## -parameters

### -param SID [in]

The service ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtunerequest">IDVBTuneRequest Interface</a>