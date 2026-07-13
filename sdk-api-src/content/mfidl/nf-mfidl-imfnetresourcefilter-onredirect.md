---
UID: NF:mfidl.IMFNetResourceFilter.OnRedirect
title: IMFNetResourceFilter::OnRedirect (mfidl.h)
description: Called when the byte stream redirects to a URL.
helpviewer_keywords: ["IMFNetResourceFilter interface [Media Foundation]","OnRedirect method","IMFNetResourceFilter.OnRedirect","IMFNetResourceFilter::OnRedirect","OnRedirect","OnRedirect method [Media Foundation]","OnRedirect method [Media Foundation]","IMFNetResourceFilter interface","mf.imfnetresourcefilter_onredirect","mfidl/IMFNetResourceFilter::OnRedirect"]
old-location: mf\imfnetresourcefilter_onredirect.htm
tech.root: mf
ms.assetid: 418EA3E0-9732-43B7-BF80-A85ECB7A9485
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter interface [Media Foundation],OnRedirect method, IMFNetResourceFilter.OnRedirect, IMFNetResourceFilter::OnRedirect, OnRedirect, OnRedirect method [Media Foundation], OnRedirect method [Media Foundation],IMFNetResourceFilter interface, mf.imfnetresourcefilter_onredirect, mfidl/IMFNetResourceFilter::OnRedirect
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
 - IMFNetResourceFilter::OnRedirect
 - mfidl/IMFNetResourceFilter::OnRedirect
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
 - IMFNetResourceFilter.OnRedirect
---

# IMFNetResourceFilter::OnRedirect


## -description

Called when the byte stream redirects to a URL.

## -parameters

### -param pszUrl [in]

The URL to which the connection has been redirected.

### -param pvbCancel [out]

To cancel the redirection, set this parameter to <b>VARIANT_TRUE</b>. To allow the redirection, set this parameter to <b>VARIANT_FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter">IMFNetResourceFilter</a>