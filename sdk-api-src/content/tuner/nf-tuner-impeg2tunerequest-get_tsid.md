---
UID: NF:tuner.IMPEG2TuneRequest.get_TSID
title: IMPEG2TuneRequest::get_TSID (tuner.h)
description: The get_TSID method retrieves the transport stream ID.
helpviewer_keywords: ["IMPEG2TuneRequest interface [Microsoft TV Technologies]","get_TSID method","IMPEG2TuneRequest.get_TSID","IMPEG2TuneRequest::get_TSID","IMPEG2TuneRequestget_TSID","get_TSID","get_TSID method [Microsoft TV Technologies]","get_TSID method [Microsoft TV Technologies]","IMPEG2TuneRequest interface","mstv.impeg2tunerequest_get_tsid","tuner/IMPEG2TuneRequest::get_TSID"]
old-location: mstv\impeg2tunerequest_get_tsid.htm
tech.root: mstv
ms.assetid: 971e2643-e68f-4b4c-86e0-2e20e2f8a88c
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequest interface [Microsoft TV Technologies],get_TSID method, IMPEG2TuneRequest.get_TSID, IMPEG2TuneRequest::get_TSID, IMPEG2TuneRequestget_TSID, get_TSID, get_TSID method [Microsoft TV Technologies], get_TSID method [Microsoft TV Technologies],IMPEG2TuneRequest interface, mstv.impeg2tunerequest_get_tsid, tuner/IMPEG2TuneRequest::get_TSID
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMPEG2TuneRequest::get_TSID
 - tuner/IMPEG2TuneRequest::get_TSID
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
 - IMPEG2TuneRequest.get_TSID
---

# IMPEG2TuneRequest::get_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TSID</b> method retrieves the transport stream ID.

## -parameters

### -param TSID [out]

Pointer to a variable that receives the transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2tunerequest">IMPEG2TuneRequest Interface</a>