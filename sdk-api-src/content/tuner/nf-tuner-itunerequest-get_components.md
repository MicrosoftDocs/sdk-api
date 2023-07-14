---
UID: NF:tuner.ITuneRequest.get_Components
title: ITuneRequest::get_Components (tuner.h)
description: The get_Components method retrieves the components contained in this tune request.
helpviewer_keywords: ["ITuneRequest interface [Microsoft TV Technologies]","get_Components method","ITuneRequest.get_Components","ITuneRequest::get_Components","ITuneRequestget_Components","get_Components","get_Components method [Microsoft TV Technologies]","get_Components method [Microsoft TV Technologies]","ITuneRequest interface","mstv.itunerequest_get_components","tuner/ITuneRequest::get_Components"]
old-location: mstv\itunerequest_get_components.htm
tech.root: mstv
ms.assetid: f15ef4f6-ca36-4d46-93c7-26f1fbcb21cd
ms.date: 12/05/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_Components method, ITuneRequest.get_Components, ITuneRequest::get_Components, ITuneRequestget_Components, get_Components, get_Components method [Microsoft TV Technologies], get_Components method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_components, tuner/ITuneRequest::get_Components
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
 - ITuneRequest::get_Components
 - tuner/ITuneRequest::get_Components
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
 - ITuneRequest.get_Components
---

# ITuneRequest::get_Components


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Components</b> method retrieves the components contained in this tune request.

## -parameters

### -param Components [out]

Receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> interface pointer. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

A tune request always contains a collection of components, but the collection can be empty. If the component information is present in the transport stream tables, a Guide Store loader can obtain the information from the TIF and include it in the tune request at the time it creates it.

If the method succeeds, the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> interface has an outstanding reference count. The caller must release the interface.

After a tune request is submitted to the Network Provider filter, the Network Provider updates the component lists in the tune request. You can get the updated component list by calling <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-get_tunerequest">ITuner::get_TuneRequest</a> on the Network Provider, and then calling <b>get_Components</b> on the returned tune request. (The original tune request that was submitted to the Network Provider does not get updated, because the Network Provider creates an internal copy of the tune request. Therefore, you have to call <b>get_TuneRequest</b> to get the updated component list.)

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>