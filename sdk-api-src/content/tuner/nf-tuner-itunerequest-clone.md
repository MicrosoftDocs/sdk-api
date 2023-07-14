---
UID: NF:tuner.ITuneRequest.Clone
title: ITuneRequest::Clone (tuner.h)
description: The Clone method returns a new copy of this tune request.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","ITuneRequest interface","ITuneRequest interface [Microsoft TV Technologies]","Clone method","ITuneRequest.Clone","ITuneRequest::Clone","ITuneRequestClone","mstv.itunerequest_clone","tuner/ITuneRequest::Clone"]
old-location: mstv\itunerequest_clone.htm
tech.root: mstv
ms.assetid: 14298e56-805d-48f3-9f78-79d4eaf2239f
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ITuneRequest interface, ITuneRequest interface [Microsoft TV Technologies],Clone method, ITuneRequest.Clone, ITuneRequest::Clone, ITuneRequestClone, mstv.itunerequest_clone, tuner/ITuneRequest::Clone
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
 - ITuneRequest::Clone
 - tuner/ITuneRequest::Clone
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
 - ITuneRequest.Clone
---

# ITuneRequest::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method returns a new copy of this tune request.

## -parameters

### -param NewTuneRequest [out]

Address of an <b>ITuneRequest</b> interface pointer that will be set to the new object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method performs a "deep copy" of the object; in other words it copies all sub-objects as well, including <a href="/previous-versions/windows/desktop/mstv/components-object">Components</a>, <a href="/previous-versions/windows/desktop/mstv/languagecomponenttype-object">LanguageComponentType</a> objects, and so on.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>