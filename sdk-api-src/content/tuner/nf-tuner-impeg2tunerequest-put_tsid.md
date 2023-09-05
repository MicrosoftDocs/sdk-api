---
UID: NF:tuner.IMPEG2TuneRequest.put_TSID
title: IMPEG2TuneRequest::put_TSID (tuner.h)
description: The put_TSID method sets the transport stream ID.
helpviewer_keywords: ["IMPEG2TuneRequest interface [Microsoft TV Technologies]","put_TSID method","IMPEG2TuneRequest.put_TSID","IMPEG2TuneRequest::put_TSID","IMPEG2TuneRequestput_TSID","mstv.impeg2tunerequest_put_tsid","put_TSID","put_TSID method [Microsoft TV Technologies]","put_TSID method [Microsoft TV Technologies]","IMPEG2TuneRequest interface","tuner/IMPEG2TuneRequest::put_TSID"]
old-location: mstv\impeg2tunerequest_put_tsid.htm
tech.root: mstv
ms.assetid: 47212dc7-601e-4b38-953e-a6b84e73fafa
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequest interface [Microsoft TV Technologies],put_TSID method, IMPEG2TuneRequest.put_TSID, IMPEG2TuneRequest::put_TSID, IMPEG2TuneRequestput_TSID, mstv.impeg2tunerequest_put_tsid, put_TSID, put_TSID method [Microsoft TV Technologies], put_TSID method [Microsoft TV Technologies],IMPEG2TuneRequest interface, tuner/IMPEG2TuneRequest::put_TSID
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
 - IMPEG2TuneRequest::put_TSID
 - tuner/IMPEG2TuneRequest::put_TSID
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
 - IMPEG2TuneRequest.put_TSID
---

# IMPEG2TuneRequest::put_TSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TSID</b> method sets the transport stream ID.

## -parameters

### -param TSID [in]

Specifies the transport stream ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2tunerequest">IMPEG2TuneRequest Interface</a>