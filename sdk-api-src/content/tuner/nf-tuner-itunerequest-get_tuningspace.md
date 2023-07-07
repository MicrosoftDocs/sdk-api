---
UID: NF:tuner.ITuneRequest.get_TuningSpace
title: ITuneRequest::get_TuningSpace (tuner.h)
description: The get_TuningSpace method retrieves the tuning space that was used to create this tune request.
helpviewer_keywords: ["ITuneRequest interface [Microsoft TV Technologies]","get_TuningSpace method","ITuneRequest.get_TuningSpace","ITuneRequest::get_TuningSpace","ITuneRequestget_TuningSpace","get_TuningSpace","get_TuningSpace method [Microsoft TV Technologies]","get_TuningSpace method [Microsoft TV Technologies]","ITuneRequest interface","mstv.itunerequest_get_tuningspace","tuner/ITuneRequest::get_TuningSpace"]
old-location: mstv\itunerequest_get_tuningspace.htm
tech.root: mstv
ms.assetid: 6952df72-30f3-4c33-a0bf-d2ad8022042c
ms.date: 12/05/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_TuningSpace method, ITuneRequest.get_TuningSpace, ITuneRequest::get_TuningSpace, ITuneRequestget_TuningSpace, get_TuningSpace, get_TuningSpace method [Microsoft TV Technologies], get_TuningSpace method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_tuningspace, tuner/ITuneRequest::get_TuningSpace
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
 - ITuneRequest::get_TuningSpace
 - tuner/ITuneRequest::get_TuningSpace
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
 - ITuneRequest.get_TuningSpace
---

# ITuneRequest::get_TuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TuningSpace</b> method retrieves the tuning space that was used to create this tune request.

## -parameters

### -param TuningSpace [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a> interface. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

You must first access the tuning space in order to obtain the default locator and the default preferred component types.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>