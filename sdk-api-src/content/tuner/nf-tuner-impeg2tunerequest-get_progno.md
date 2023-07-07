---
UID: NF:tuner.IMPEG2TuneRequest.get_ProgNo
title: IMPEG2TuneRequest::get_ProgNo (tuner.h)
description: The get_ProgNo method retrieves the program number ID.
helpviewer_keywords: ["IMPEG2TuneRequest interface [Microsoft TV Technologies]","get_ProgNo method","IMPEG2TuneRequest.get_ProgNo","IMPEG2TuneRequest::get_ProgNo","IMPEG2TuneRequestget_ProgNo","get_ProgNo","get_ProgNo method [Microsoft TV Technologies]","get_ProgNo method [Microsoft TV Technologies]","IMPEG2TuneRequest interface","mstv.impeg2tunerequest_get_progno","tuner/IMPEG2TuneRequest::get_ProgNo"]
old-location: mstv\impeg2tunerequest_get_progno.htm
tech.root: mstv
ms.assetid: dde8979a-633d-4fc4-b31e-bdd43823db6a
ms.date: 12/05/2018
ms.keywords: IMPEG2TuneRequest interface [Microsoft TV Technologies],get_ProgNo method, IMPEG2TuneRequest.get_ProgNo, IMPEG2TuneRequest::get_ProgNo, IMPEG2TuneRequestget_ProgNo, get_ProgNo, get_ProgNo method [Microsoft TV Technologies], get_ProgNo method [Microsoft TV Technologies],IMPEG2TuneRequest interface, mstv.impeg2tunerequest_get_progno, tuner/IMPEG2TuneRequest::get_ProgNo
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
 - IMPEG2TuneRequest::get_ProgNo
 - tuner/IMPEG2TuneRequest::get_ProgNo
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
 - IMPEG2TuneRequest.get_ProgNo
---

# IMPEG2TuneRequest::get_ProgNo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ProgNo</b> method retrieves the program number ID.

## -parameters

### -param ProgNo [out]

Pointer to a variable that receives the program number ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2tunerequest">IMPEG2TuneRequest Interface</a>