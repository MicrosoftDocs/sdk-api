---
UID: NF:mfidl.IMFNetResourceFilter.OnSendingRequest
title: IMFNetResourceFilter::OnSendingRequest (mfidl.h)
description: Called when the byte stream requests a URL.
helpviewer_keywords: ["IMFNetResourceFilter interface [Media Foundation]","OnSendingRequest method","IMFNetResourceFilter.OnSendingRequest","IMFNetResourceFilter::OnSendingRequest","OnSendingRequest","OnSendingRequest method [Media Foundation]","OnSendingRequest method [Media Foundation]","IMFNetResourceFilter interface","mf.imfnetresourcefilter_onsendingrequest","mfidl/IMFNetResourceFilter::OnSendingRequest"]
old-location: mf\imfnetresourcefilter_onsendingrequest.htm
tech.root: mf
ms.assetid: 4FE6BBE8-A8EC-4304-BC4B-4D49F8EADC25
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter interface [Media Foundation],OnSendingRequest method, IMFNetResourceFilter.OnSendingRequest, IMFNetResourceFilter::OnSendingRequest, OnSendingRequest, OnSendingRequest method [Media Foundation], OnSendingRequest method [Media Foundation],IMFNetResourceFilter interface, mf.imfnetresourcefilter_onsendingrequest, mfidl/IMFNetResourceFilter::OnSendingRequest
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFNetResourceFilter::OnSendingRequest
 - mfidl/IMFNetResourceFilter::OnSendingRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFNetResourceFilter.OnSendingRequest
---

# IMFNetResourceFilter::OnSendingRequest


## -description

Called when the byte stream requests a URL.

## -parameters

### -param pszUrl [in]

The URL that the byte stream is requesting.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter">IMFNetResourceFilter</a>