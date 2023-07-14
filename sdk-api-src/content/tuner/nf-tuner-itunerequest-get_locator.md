---
UID: NF:tuner.ITuneRequest.get_Locator
title: ITuneRequest::get_Locator (tuner.h)
description: The get_Locator method is called from the Network Provider to get the ILocator object associated with the requested broadcast.
helpviewer_keywords: ["ITuneRequest interface [Microsoft TV Technologies]","get_Locator method","ITuneRequest.get_Locator","ITuneRequest::get_Locator","ITuneRequestget_Locator","get_Locator","get_Locator method [Microsoft TV Technologies]","get_Locator method [Microsoft TV Technologies]","ITuneRequest interface","mstv.itunerequest_get_locator","tuner/ITuneRequest::get_Locator"]
old-location: mstv\itunerequest_get_locator.htm
tech.root: mstv
ms.assetid: 9f2a000a-0133-44f4-8e9c-7d37435596d7
ms.date: 12/05/2018
ms.keywords: ITuneRequest interface [Microsoft TV Technologies],get_Locator method, ITuneRequest.get_Locator, ITuneRequest::get_Locator, ITuneRequestget_Locator, get_Locator, get_Locator method [Microsoft TV Technologies], get_Locator method [Microsoft TV Technologies],ITuneRequest interface, mstv.itunerequest_get_locator, tuner/ITuneRequest::get_Locator
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
 - ITuneRequest::get_Locator
 - tuner/ITuneRequest::get_Locator
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
 - ITuneRequest.get_Locator
---

# ITuneRequest::get_Locator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Locator</b> method is called from the Network Provider to get the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> object associated with the requested broadcast.

## -parameters

### -param Locator [out]

Address of an <b>ILocator</b> interface pointer that will be set to the new object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest Interface</a>