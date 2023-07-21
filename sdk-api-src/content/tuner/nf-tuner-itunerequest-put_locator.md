---
UID: NF:tuner.ITuneRequest.put_Locator
title: ITuneRequest::put_Locator (tuner.h)
description: The put_Locator method is called from the Network Provider to set the ILocator object associated with the requested broadcast.
helpviewer_keywords: ["ITuneRequest interface [Microsoft TV Technologies]","put_Locator method","ITuneRequest.put_Locator","ITuneRequest::put_Locator","ITuneRequestput_Locator","mstv.itunerequest_put_locator","put_Locator","put_Locator method [Microsoft TV Technologies]","put_Locator method [Microsoft TV Technologies]","ITuneRequest interface","tuner/ITuneRequest::put_Locator"]
old-location: mstv\itunerequest_put_locator.htm
tech.root: mstv
ms.assetid: 798ff904-5f08-4d3b-8a56-ca1c2df52aaf
ms.date: 12/05/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],put_Locator method, ITuneRequest.put_Locator, ITuneRequest::put_Locator, ITuneRequestput_Locator, mstv.itunerequest_put_locator, put_Locator, put_Locator method [Microsoft TV Technologies], put_Locator method [Microsoft TV Technologies],ITuneRequest interface, tuner/ITuneRequest::put_Locator
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
 - ITuneRequest::put_Locator
 - tuner/ITuneRequest::put_Locator
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
 - ITuneRequest.put_Locator
---

# ITuneRequest::put_Locator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Locator</b> method is called from the Network Provider to set the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> object associated with the requested broadcast.

## -parameters

### -param Locator [in]

Pointer to an <b>ILocator</b> interface that specifies the new locator.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>